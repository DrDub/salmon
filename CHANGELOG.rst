3.0-dev
=======

- Removed lots of cruft (#19)
- Moved from modargs to argparse - command line interface has changed (#28)
  * Improved tests for command line (#47)
- Moved from PyDNS to dnspython
- Tests can now be run without having to start a log-server first (#6)
- MailRequest objects are now wrappers around Python's ``email.message.Message`` class. (#40)
  * Deserializing incoming messages is now done in a slightly more lazy fashion
  * Also allows access to the "pristine" ``Message`` object without having to back-convert
  * Header setting now replaces by default (#44)
- End support of Python 2.6 (#42)
- Settings no longer limited to per app "config" module (#38)
- Allow ``salmon.server.Relay`` to talk to LMTP servers (#41)
- Make ``LMTPReceiver`` the default in the prototype app (#48)
- Properly work around SMTPReceiver bug caused by Python's ``smtpd`` module (#48)
  * This means that Salmon will no longer accept multiple RCPT TOs over SMTP

Earlier Releases
================

Sorry, we didn't keep a changelog prior to Salmon 3.0!
