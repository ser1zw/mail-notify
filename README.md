# Mail notify

Notify your unread emails fetched from IMAP servers.


## Requirement
- Ruby 1.9.3
- Ubuntu 12.04
- Target mail service that allows you to access via IMAP (e.g. Gmail)


## Install
### Install Ruby 1.9.3

See [http://www.ruby-lang.org/](http://www.ruby-lang.org/).

### Install ```notify-send``` command

<pre>
$ sudo apt-get install notify-osd libnotify-bin
</pre>

## Usage
### Edit config file

Edit ```config.yml``` to set IMAP server, email, password
and interval time to fetch emails.

<pre>
server: [IMAP server]
email: [Email address]
password: [Password]
interval: [Fetch interval time (seconds)]
</pre>

Example for using Gmail:
<pre>
server: imap.gmail.com
email: your-email@gmail.com
password: your_password
interval: 300
</pre>

### Run the script

<pre>
$ ruby mail-notify
</pre>

### Stop the script

```mail-notify``` works as a daemon.

To kill the process, check the PID and kill it.
<pre>
$ pgrep -fl mail-notify
16500 ruby ./mail-notify
$ kill -KILL 16500
</pre>
Or shortly,
<pre>
$ pkill -f mail-notify
</pre>

## License

This project is released under the MIT license:

[http://opensource.org/licenses/MIT](http://opensource.org/licenses/MIT)

