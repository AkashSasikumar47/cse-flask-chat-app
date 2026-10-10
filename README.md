# Flask Chat App

A simple shared chat room in Flask: anyone who opens the page can post, and everyone sees the same messages.

> College mini-project · Computer Science and Engineering, SRMIST · Cloud Computing · December 2023

## Features

- One page with the message list and a form for your name and message
- Names and messages are trimmed and length-limited (50 and 500 characters)
- Keeps the last 100 messages
- A small JSON endpoint lists everyone who has posted

## Built with

Python 3, Flask and Jinja templates.

## Run it

```bash
python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
python app.py
```

Open http://127.0.0.1:5000 in a browser.

## How it works

Messages live in memory, so they reset when the server restarts. `/send` takes the form post and redirects back to the page, and `/get_users` returns the list of names as JSON. Jinja escapes every name and message when the page is rendered, so posted HTML is shown as text.

## Project structure

```
app.py                 Flask routes and the in-memory message list
templates/index.html   the chat page
requirements.txt       Flask
```

## License

[MIT](LICENSE)
