# Fire

These are instructions for a demo of a token that degrades over time.

There are two test environments of the app:

- The standard version of the app.
- A version where tokens degrade much faster, in hours instead of days. [See below](#degradation) on how degradation works.

These instructions assume the use of the fast environment, and all URLs will point to it, but everything except the speed of degradation works the same on both.

## Testing instructions

### Registering

First you'll need an account. Open the website, and click Register. You can register for an account using your email address.

After registering, you'll receive an email to confirm your account. Before confirming, you should not be able to log in. This step and the reCAPTCHA checkbox are for discouraging automated signups.

Once you've clicked the confirmation link, you can sign in. This is also when you'll be transferred a signup bonus of 50 FIRE to get you started. Depending on the speed of the blockchain currently, you may already see the bonus when you sign in, or it may take a few minutes.

### Wallet screen

Once logged in, you'll be taken to the main wallet screen. This will show you your account address, current token balance, and a history of transactions. The first time you log in, the transactions will naturally be empty.

There are a few things you can do here:

- Clicking on your own account's address will bring up a token transfer history for that account. You should see the 50 FIRE bonus incoming from 0x0.
- Clicking on the token's name under Token Balance will bring up the transfer history for the token as a whole.
- Once you have transactions, clicking one will bring up the details of that transaction.
- Clicking Send Tokens will open the token transfer screen.
- Clicking Stake will open the dialog to stake 100 FIRE.

### Sending tokens

The Send Tokens screen will let you send FIRE to either an email address, or a wallet address.

When sending to an email address, one of two things will happen:

1. If that email address has signed up for the app already, their default account will be the recipient.
2. If no account is found, the email address will be sent an invitation to register.

### Staking

Once you have enough FIRE, you can spend 100 tokens to receive stake. For testing purposes, all staking does right now is mark you as having staked, but it'll be tied to functionality in the future.

## Invitation and referrals

As mentioned in the previous section, sending tokens to an email address that doesn't have an account will produce an invitation.

If that person then registers an account, you will receive bonus FIRE that's equal to two-thirds (67%) of what you sent them. For example, if you send 10 FIRE and the recipient registers, you'll receive 6.7 FIRE.

Furthermore, if that person then invites others using the same method, you will get another bonus of 50%, up to 3 times. In other words, it's possible to receive more than double the FIRE you sent as bonuses.

These bonuses are capped so that only up to 25 FIRE is counted. If you send 25 FIRE, and receive all possible bonuses, you'll get 54.25 FIRE in return, netting you 29.25 FIRE total.

## Degradation

FIRE tokens degrade over time if the account has no activity, and your account will eventually fall to 0 balance unless you do something with the tokens.

For testing purposes, the only actions you can take are transferring tokens and staking.

In the normal version, degradation happens as follows:

- After one day of no activity, you'll lose 1 token, and an additional token per day up to 5 days.
- Starting on the 6th day you will lose 2 tokens per day, until you've lost 15 tokens at the end of day 10.
- After 10 days, you'll lose one token every two hours until you've lost 30 tokens.
- If there's still no activity, you'll lose one token per hour until your balance is 0.

In the fast testing version, swap days to hours, and hours to minutes.

In the normal version, you'll also receive a two day grace period of no degradation after signing up, and additional three day grace periods when your invitees register for an account.

