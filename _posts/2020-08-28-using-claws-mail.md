---
title: "Using Claws Mail Client"
date: 2020-08-28
comments: true
category: Technology
permalink: "/:title.html"
---

![Claws Mail](assets/2020-08-28/0.png)

## Contents

- [Why](#why)
- [Install](#install)
- [Add Account](#add-account)
- [Compose Email](#compose-email)
- [FAQ](#faq)

## Why?

Why use an email-client? I do not know. Except that using an external
email-client seems like a grown-up thing to do, like owning a wallet.

Why use Claws Mail? I guess because it uses less resource than others.
But, having a modern computer, that sounds more like an excuse than a
valid reason.

Basically, the reason will depend on the user. I will not try and
convince you to use Claws Mail. But if you do decide to use it, this
blogpost should be a good enough tutorial to begin.

## Install

Use your preferred method of installation. The client should be
available in your package-manager's respository. If not, you can
always manually build and install from the [git repository][1].

## Add Account

Go to `Configuration > Create new account` and you should be presented
with the following window.

![Create new account](assets/2020-08-28/1.png)

1. **Basic**:

    Enter your name, email address, and name of the account. Check the
    `Set as default` option if it is to be your default account.

    Choose your preferred protocol. It should be either POP or IMAP.
    If you do not know what these are, head on to [this website][2].

    Click the Auto-configure button. If your email address is one of
    the popular ones, e.g. Gmail or Yahoo, the servers and user-id
    should be filled up automatically now. If you get an error, I am
    afraid you would have to look through the manual of your email
    provider and figure out those information manually.

    If you decide not to put in the password of your email account
    because of worry over security, you may skip it. Then you would
    have to enter it every time you reset the cache.

2. **Receive**:

    Head on over to the Receive tab. Check `'Get Mail' checks for new
    messages on this account`.

3. **Send**:

    Go over to the Send tab. If your user-id and password for sending
    emails are different from those for receiving, then fill those
    options. Otherwise, leave everything as is.

4. **Advanced**:

    Move over to the Advanced tab. The ports for SMTP and IMAP should
    be filled up. If not, google for the ports specific to your email
    provider. (For Gmail, you can find the information [here][3].)

5. **Others**:

    The options for all the other tabs are self-explanatory, and
    varies depending on the demand of the user. If you are a regular
    email user, you should not have to change any of them. And if you
    are an advanced user, you already know what you would have to
    change.

Now, click on the OK button. You should see the following window.

![Claws Mail](assets/2020-08-28/2.png)

There is a problem, though: it shows your account has zero emails.
That is because you have not pulled your emails down. To do that,
right click on the account, and select `Rebuild folder tree`.

There! You should see your emails now.

![Claws Mail](assets/2020-08-28/3.png)

You might see there are duplicate folders for drafts and trash and
sent mails. It is because Claws Mail automatically creates those
folders when creating an account, while Gmail already has those
folders. To get around it, you need to right click each of those three
folders under `[Gmail]` and click `Properties` and change the folder
type to that of the corresponding folder. For example: for Trash
folder, select folder-type Trash; for Drafts folder, select Drafts;
for Sent Mail folder, select Outbox. Then delete the three duplicate
folders outside the `[Gmail]` category. That's it! You should now have
a clean folder structure.

You can add as many accounts you want. I use one for my personal use
and one for my school. My client looks like the one below.

![Claws Mail](assets/2020-08-28/4.png)

## Compose Email

To write an email, click the Compose button. The following window
should pop up.

![Compose](assets/2020-08-28/5.png)

1. **Header**:

    Fill the sender and receiver options, and write your email. You
    can also add Cc or Bcc.

    When you enter the email address for the receiver, a new option
    will pop for entering another email address. If you want to send
    the email to multiple people, you can do it this way. Otherwise,
    leave the option blank.

    If you have email addresses saved in your address book, you can
    autocomplete the address by tapping tab on your keyboard. The way
    to use the address book will be discussed in a later section.

1. **Attachment**:

    To attach a file, click the Attach button and select the files.
    You can edit or remove it in the Attachment tab.

1. **Others**:

    In the Others tab, check the option for saving the message to your
    outbox folder, which for Gmail would be the Sent Mail folder.

Now, click the Send button to send the email, or the Send later button
to queue the email, or the Draft button to save the email in the
Drafts folder. The compose window should close automatically once the
email is sent, or queued, or saved.

&nbsp;

## FAQ

### Cannot use my Gmail account

You probably need to enable less secure apps for your Google account.
Check out [this site][4] to learn how to do that.

### Incomplete emails saved in Gmail while composing

A default setting in Claws Mail saves emails to the drafts folder
every few characters while composing. Gmail uses a single folder for
storing all its emails, the one called All Mail. And the Conversation
View in Gmail makes the drafts visible.

To fix this, all you need to do is open `Configuration > Preferences`,
and go to the Writing tab under Compose category, and uncheck the
option for automatically saving messages to Drafts every few seconds.



[1]: https://git.claws-mail.org/

[2]: https://www.name.com/support/articles/205935497-Understanding-the-difference-between-POP-and-IMAP

[3]: https://support.google.com/mail/answer/7126229?hl=en

[4]: https://hotter.io/docs/email-accounts/secure-app-gmail/
