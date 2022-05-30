## Dual-mode Telegram bot

This Telegram bot was developed to be used by Telegram channel. The bot helps holders of the Telegram channels to host contests and gets statistics and other data after. This particular bot was designed especially for customer and his needs.

I will give you the simpliest and at the same time crucial table for the bot:
Participant Mode   | Admin Mode
---                | ---
Participant Access | Admin Access
---                | Owner Access

![alt text](https://github.com/isishere/kk-contests-bot/blob/main/access_circles.jpg)


### Participant Mode
Mode appears automatically if user does not have admin's or owner's rights (I will clarify on it a little later).
This mode implements in regular check: whether prospective participant remains follower of the channel or not.

#### More precisely:
Code checks user's id number `if menu.check_owner(message.from_user.id) or menu.check_admin(message.from_user.id):` after you sent it command "/start" in the chat. The first part (if theese two are true statements) corresponds to "OWNER ACCSSE" (that actually includes admin access in it), the other section that is after `else:` refers to "PART ACCESS" (Participant Access)
