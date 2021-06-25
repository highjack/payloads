Reference: https://twitter.com/jschauma/status/1378172844169961477

 # MTAs generally don't relay them any more, but most seem to accept and deliver to user@final.domain.
@1st.relay,@2nd.relay:user@final.domain

# Your MTA will probably reject this as an attempt to relay, but, hey, it's valid, although RFC5321 does not tell you to treat "!" special.
relay.domain!user@domain

# Try it out and see if your MTA will try to deliver to "final.domain" or "1st.relay"...
user%final.domain@1st.relay
'*+-/=?^_`{|}~#$@netmeister.org # RFC5321 allows all sorts of punctuation.

#the following are treted as the same by Gmail and Outlook
jdoe@domain
jdoe+whatever@domain
jdoe+somethingelse@domain
.jdoe@domain
jdoe.@domain
jd..oe@domain

#if we can quote things, then we can do all sorts of other shenanigans, and call these valid, too:

" "@netmeister.org
"<>"@netmeister.org
"put a literal escaped newline here\^M <--"@domain
