# Mailcatcher Docker Image
## What is Mailcatcher
> Catches mail and serves it through a dream.
> MailCatcher runs a super simple SMTP server which catches any message sent to it to display in a web interface.
> Run mailcatcher, set your favourite app to deliver to smtp://127.0.0.1:1025 instead of your default SMTP server, then check out http://127.0.0.1:1080 to see the mail that's arrived so far.

[MailCatcher](http://mailcatcher.me/)

## Usage
There are two exposed ports.

- 25: SMTP server
- 80: Web interface to see the mail that's arrived

Run mailcatcher process:

```
docker run -d -p 1080:80 --name mailcatcher heathrow/mailcatcher
```

Link to another container to send emails:

```
docker run -it --link mailcatcher ...
```
