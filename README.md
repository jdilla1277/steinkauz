# steinkauz
A simple json file to enable emailing from CustomGPTs

To do this you’ll need:
* A free send grid account (you can sign up [here](https://signup.sendgrid.com/)).
* An email address you want to use
* Access to CustomGPTs

## Things to be aware of:
1. **It is possible to spam people with this**. Don’t do that! Also, SendGrid has spam prevention systems in place and pretty soon your email will end up in people’s spam folders never to be seen again. Also, life is too short. Put that energy into something productive.
2. **If after setting this up, you make your CustomGPT public, people will be able to send emails using your email address paid for by you.** This is probably not what you want!

## Get set up with SendGrid
1. You’ll need to verify your email address with SendGrid, which you can do here: https://app.sendgrid.com/settings/sender_auth. It’s pretty self explanatory and they have [good docs](https://docs.sendgrid.com/ui/managing-contacts/email-address-validation).
2. Create a SendGrid API key and hold onto it, you’ll need it in a second. You can do that here: https://app.sendgrid.com/settings/api_keys

**Note:** SendGrid is free for up to 100 emails a month, beyond that you’ll need to pay.

## Create a CustomGPT
1. Go to create a CustomGPT(https://chat.openai.com/gpts/editor)
2. Go to the configure tab
3. Go to add actions
4. Import the json file: You can place this [link](https://www.jdilla.xyz/steinkauz) in the import schema field or copy and paste from this [github file](https://github.com/jdilla1277/steinkauz/blob/main/steinkauz.json) into the OpenAI action schema.
7. Add your API key to the authentication field with auth type **Bearer**. Save your action.
8. In the Instructions field for your CustomGPT, instruct your CustomGPT on how to use the email action. It’s super important that you tell it to only use your verified email address, otherwise you’ll get errors from the SendGrid API, but I also give it a sender name to make things appear a little nicer in my inbox. When you’re done, save the CustomGPT.

**My instructions**
> When using the api.sendgrid.com action to send emails, always use the email address <<TheEmailAddressYouVerifiedAbove@example.com>> no matter what. The best sender name to use is <Name You Prefer to be Called>. 

## Send an email
1. Start using ChatGPT as you normally would. When you want to email something, prompt it to do so.
2. You’ll get a dialog making sure you’re okay with CustomGPT taking this action. Make sure to press “

Now start using the CustomGPT. When you want to email something, just tell ChatGPT you want to send it. You’ll get a little pop up asking if you’re okay with the app taking this action. Once you confirm, your email will get sent.

