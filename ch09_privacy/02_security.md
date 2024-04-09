# Security

While we have our concerns about the privacy of our information, we often share it with social media platforms under the understanding that they will hold that information securely. But social media companies often fail at keeping our information secure.

For example, the proper security practice for storing user passwords is to use a [special individual encryption process](https://en.wikipedia.org/wiki/Salt_(cryptography)) {cite:p}`SaltCryptography2023` for each individual password. This way the database can only confirm that a password was the right one, but it can't independently look up what the password is or even tell if two people used the same password. Therefore if someone had access to the database, the only way to figure out the right password is to use "brute force," that is, keep guessing passwords until they guess the right one (and [each guess takes a lot of time](https://stackoverflow.com/a/15763243) {cite:p}`linacAnswerBcryptPassword2013`).

But while that is the proper security for storing passwords. So for example, [Facebook stored millions of Instagram passwords in plain text](https://www.theverge.com/2019/4/18/18485599/facebook-instagram-passwords-plain-text-millions-users) {cite:p}`kastrenakesFacebookStoredMillions2019`, meaning the passwords weren't encrypted and anyone with access to the database could simply read everyone's passwords. And Adobe encrypted their passwords improperly and then [hackers leaked their password database of 153 million users](https://www.explainxkcd.com/wiki/index.php/1286:_Encryptic) {cite:p}`1286EncrypticExplain`.

From a security perspective there are many risks that a company faces, such as:
- Employees at the company misusing their access, like [Facebook employees using their database permissions to stalk women](https://www.themarysue.com/facebook-employees-abused-access-target-women/) {cite:p}`haleNewBookSays2021`
- Hackers finding a vulnerability and inserting, modifying, or downloading information. For example:
  - hackers stealing the [names, Social Security numbers, and birthdates of 143 million Americans from Equifax](https://en.wikipedia.org/wiki/2017_Equifax_data_breach) {cite:p}`2017EquifaxData2023`
  - hackers posting publicly the [phone numbers, names, locations, and some email addresses of 530 million Facebook users](https://www.npr.org/2021/04/09/986005820/after-data-breach-exposes-530-million-facebook-says-it-will-not-notify-users) {cite:p}`bowmanDataBreachExposes2021`, or about 7% of all people on Earth

Hacking attempts can be made on individuals, whether because the individual is the goal target, or because the individual works at a company which is the target. Hackers can target individuals with attacks like:
- Password reuse attacks, where if they find out your password from one site, they try that password on many other sites
- Hackers tricking a computer into thinking they are another site, for example:
  - the [US NSA impersonated Google](https://slate.com/technology/2013/10/nsa-smiley-face-muscular-spying-on-google-yahoo-speaks-volumes-about-agency-s-attitude.html) {cite:p}`oremusCelebrateSpyingGoogle2013`
- [Social engineering](https://en.wikipedia.org/wiki/Social_engineering_(security)) {cite:p}`SocialEngineeringSecurity2023`, where they try to gain access to information or locations by tricking people. For example:
  - Phishing attacks, where they make a fake version of a website or app and try to get you to enter your information or password into it. Some people have made [malicious QR codes to take you to a phishing site](https://www.pcmag.com/news/fbi-hackers-are-compromising-legit-qr-codes-to-send-you-to-phishing-sites) {cite:p}`FBIHackersAre`.
  - Many of the actions done by the con-man [Frank Abagnale](https://en.wikipedia.org/wiki/Frank_Abagnale) {cite:p}`FrankAbagnale2023`, which were portrayed in the movie [Catch Me If You Can](https://www.imdb.com/title/tt0264464/) {cite:p}`spielbergCatchMeIf2002`

% TODO: - Tricking users into running code: - Open developer tools console with https://www.facebook.com/ and see the warning

One of the things you can do as an individual to better protect yourself against hacking is to enable [2-factor authentication](https://en.wikipedia.org/wiki/Multi-factor_authentication) {cite:p}`MultifactorAuthentication2023` on your accounts.
