from watchdog.observers import Observer
from watchdog.events import FileSystemEventHandler
import os
import time

class ReloadHandler(FileSystemEventHandler):
    def on_modified(self, event):
        if event.src_path.endswith(".py"):
            print(f'Change detected in {event.src_path}. Restarting Flask app...')
            os.system("flask run --host=0.0.0.0 --port=5000")

if __name__ == "__main__":
    # Directory to monitor (current directory where the app is running)
    path = "/app"  
    event_handler = ReloadHandler()
    observer = Observer()
    observer.schedule(event_handler, path, recursive=True)
    observer.start()
    
    try:
        while True:
            time.sleep(1)
    except KeyboardInterrupt:
        observer.stop()
    observer.join()
