from flask import Flask, render_template, request
import wolframalpha

app = Flask(__name__)

# WolframAlpha API key
app_id = 'YOUR_APP_ID'

# Route to display the input form and show results
@app.route('/', methods=['GET', 'POST'])
def index():
    result = None
    if request.method == 'POST':
        # Get form data
        number_of_printers = int(request.form['number_of_printers'])
        sheets_per_printer_per_day = int(request.form['sheets_per_printer_per_day'])
        buffer_percentage = float(request.form['buffer_percentage']) / 100
        
        # Query WolframAlpha for number of working days in the last 30 days
        client = wolframalpha.Client(app_id)
        query = 'number of working days in the last 30 days'
        res = client.query(query)
        working_days = int(next(res.results).text)
        
        # Perform the paper requirement calculations
        sheets_per_ream = 500
        reams_per_case = 10

        total_sheets = number_of_printers * sheets_per_printer_per_day * working_days
        total_reams = total_sheets / sheets_per_ream
        total_cases = total_reams / reams_per_case
        total_cases_with_buffer = total_cases * (1 + buffer_percentage)

        # Round the final result
        result = {
            'working_days': working_days,
            'total_sheets': total_sheets,
            'total_reams': total_reams,
            'total_cases': total_cases,
            'total_cases_with_buffer': round(total_cases_with_buffer, 2)
        }
    
    # Render the form and results
    return render_template('index.html', result=result)

if __name__ == '__main__':
    app.run(debug=True)
