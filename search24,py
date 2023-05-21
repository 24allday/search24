#Search24.py
#By 24bkdoor
#Search24 in python
#Part of 24 Recon Project
#importing modules
import requests
import time

#define colours
def bg(colour):
    def inbg(msg):
        print(f'{colour}{msg}')
    return inbg

GREEN = bg('\033[92m')
YELLOW = bg('\033[93m')
RED = bg('\033[91m')

#Search username and apply relevant pauses
def search(username):
    YELLOW(f' Searching for username: {username}')
    time.sleep(0.5)
    print('.......')
    time.sleep(0.5)
    print('.......\n')
    time.sleep(0.5)
#notification that the process has begun
    YELLOW(f' Hunting the hunter ;<[ \n')
    time.sleep(0.5)
    print('.......')
    time.sleep(0.5)
    print('.......\n')
    time.sleep(0.5)

    time.sleep(1)
#matching
    count = 0
    match = True
#website list amend how you wish
    # Websites
    instagram = f'https://www.instagram.com/{username}'
    facebook = f'https://www.facebook.com/{username}'
    twitter = f'https://www.twitter.com/{username}'
    youtube = f'https://www.youtube.com/{username}'
    # Rest of the websites...

    WEBSITES = [instagram, facebook, twitter, youtube]

    for url in WEBSITES:
        r = requests.get(url)

        if r.status_code == 200:
            if match:
                GREEN(' FOUND MATCHES :<}')
                match = False
            YELLOW(f'\n{url} - {r.status_code} - OK')
            if username in r.text:
                GREEN(f'POSITIVE MATCH: Username:{username} - text has been detected in the URL. Go ahead and explore further')
            else:
                GREEN(f'POSITIVE MATCH: Username:{username} - \033[91mtext has NOT been detected in the URL, could be a FALSE POSITIVE.')
        count += 1

    total = len(WEBSITES)
    GREEN(f'FINISHED: A total of {count} MATCHES found out of {total} websites :<] ')


if __name__ == '__main__':
    username = input("\033[34m{+} Enter username to search and we will beging Search24 ==> ")
    search(username)
