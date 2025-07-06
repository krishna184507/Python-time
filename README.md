# Python-time
Basic Python program to say good morning,  afternoon, evening by timestamp
import time

def get_greeting():
    current_time = time.localtime()
    hour = current_time.tm_hour

    if 4 <= hour < 12:
        return "Good Morning"
    elif 12 <= hour < 17:
        return "Good Afternoon"
    elif 17 <= hour < 21:
        return "Good Evening"
    else:
        return "Good Night"

def main():
    timestamp = time.strftime('%H:%M:%S')
    print(f"Current Time: {timestamp}")
    greeting = get_greeting()
    print(greeting)

if __name__ == "__main__":
    main()
