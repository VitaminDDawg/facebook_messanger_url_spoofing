Title

URL and thumbnail impersonation attack via Facebook messenger and linkshim "bypass"
![shimmed-message](https://github.com/VitaminDDawg/facebook_messanger_url_spoofing/assets/116259185/f54cc352-c0d3-4207-b1e2-58ed3a2bae5d)

Vuln Type
Other

Product Area
Messenger

Description/Impact
• Links within Facebook messenger do not display endpoint urls in their previews/thumbnails as they do
normally within the public Facebook web&app interface leading to user "confusion".

• External urls can be masked via a linkshim url and a modified website siteid, tagline and logo.

• Linkshim urls copied from a private "only me" setting wall post acquire their own personal linkshim url when
pasted in full via messenger.

• When the user interacts with the link they received they are served their own linkshim url and redirected off-
site without a notice that they are leaving facebook.com.

• After X amount of time (12h?-24h?) the shimmed link becomes "invalid" and issues a warning to the user
that they are leaving the parent site.

• Confirmed against test accounts and real account, website and android app. "poc-selftest.mp4" is a self test on android.

users at risk of impersonation attacks
Repro Steps
Mobile app version: 421.0.0.12.61

1. Create external host with siteid, tagline and logo matching Facebook

2. Post url privately on wall via the "only me" setting

3. Copy linkshim url from private post

4. Paste linkshim url to messenger and send to secondary test account

5. Receive link matching "l.facebook.com" with valid looking thumbnail and no indication of the real endpoint url on secondary test account.

6. On secondary test account click link. You will be redirected through personal linkshim and sent directly to external domain with no notification.

7.(if original linkshim is "old" user is alerted to domain exit)
