### Making text appear one character at a time.

    import sys, time
  
    def print1by1(text, delay=0.1):
        for c in text:
            sys.stdout.write(c)
            sys.stdout.flush()
            time.sleep(delay)
        print

    print1by1("Hello there!")
    
### Fill screen with random colorful strings

    # python3 -m pip install asciimatics
    from random import randint
    from asciimatics.screen import Screen

    def demo(screen):
        while True:
            screen.print_at('Hello world!',
                            randint(0, screen.width), randint(0, screen.height),
                            colour=randint(0, screen.colours - 1),
                            bg=randint(0, screen.colours - 1))
            ev = screen.get_key()
            if ev in (ord('Q'), ord('q')):
                return
            screen.refresh()

    Screen.wrapper(demo)
    
### Clear screen while still in program

    from subprocess import call
    from os import name as osname

    def clear():
        # check and make call for specific operating system
        call('clear' if osname =='posix' else 'cls')
