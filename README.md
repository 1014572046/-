from time import sleep
import os

def pomodoro(minutes):
    seconds = minutes * 60
    while seconds > 0:
        seconds -= 1
        minutes, sec = divmod(seconds, 60)
        timer = '{:02d}:{:02d}'.format(minutes, sec)
        print(timer + ' | Press Ctrl+C to stop.')
        sleep(1)
        os.system('clear')  # For windows, use 'cls' instead
    print('Time is up!')
