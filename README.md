# Gmail Newsletter Filter
A Gmail filter that will **catch newsletters** and **clear your inbox**.

## The query

```
(unsubscribe OR from:noreply OR from:no-reply OR "[New Article]" OR "[Nuovo Articolo]" OR "[New Post]" OR "make sure you keep getting these emails" OR "this email was sent to" OR "turn off these emails" OR "You’ve received this email because" OR "per visualizzare questa email" OR "Hai ricevuto questa email perché" -{"confirm your" mailbrew subject:urgent subject:alert label:notifications})
```

Among other things, this query will **include** email with:
* "Unsubscribe" anywhere
* Patterns like "You've received this email because" or "To view this email"
* Subjets like "[New Article]"

It will **exclude**:
* Emails with keywords like "urgent" or "alert"
* [Mailbrew](https://mailbrew.com) digests
* Emails with label `notifications` (you can change it to any label)

The query includes a few Italian sentences as well.

## Usage

To add this filter to your gmail, copy the string above, customize it, and then add it to this URL:

`https://mail.google.com/mail/u/0/#create-filter/has=`

Then click **Continue**, and in the final screen, check:
* **Skip the Inbox (Archive it)**
* **Apple the label: `Newsletters`**

If you want to already clear your inbox, also check:
* **Also apply filter to matching conversations.**

Now, in any email client you use, you'll find your newsletters in the dedicated label Newsletters, and you'll read them when you want, keeping your inbox clean.

## Feedback and Contributions

Feel free to contribute to the filter with other common patterns, and to say hy or give feedback [hit me up on Twitter](https://twitter.com/linuz90).

For more email goodies, check out [inboxze.ro](https://inboxze.ro).
