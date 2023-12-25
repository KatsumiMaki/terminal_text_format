import re
import sys
import tty
import termios

def process_text(text):
    # Replace [\r\n] with space
    text = re.sub(r'[\r\n]', ' ', text)

    # Replace two spaces with \n\n
    text = re.sub(r'  ', '\\n\\n', text)

    # Replace two spaces with one space
    # text = re.sub(r'  ', ' ', text)

    return text

def get_user_input():
    sys.stdout.flush()
    user_text = ''

    try:
        old_settings = termios.tcgetattr(sys.stdin)
        tty.setraw(sys.stdin.fileno())

        while True:
            c = sys.stdin.read(1)
            if c == '\n' or ord(c) == 3:
                break
            else:
                user_text += c

    finally:
        termios.tcsetattr(sys.stdin, termios.TCSADRAIN, old_settings)

    result = process_text(user_text)
    print("Result:")
    print(result)

    with open('output.txt', 'w') as file:
        file.write(result)

get_user_input()
