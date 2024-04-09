# Who does data fit?
Because all data is a simplification of reality, those simplifications work well for some people and some situations but can cause problems for other people and other situations.

Thus, when designers of social media systems make decisions about how data will be saved and what constraints will be put on the data, they are making decisions about who will get a better experience. Based on these decisions, some people will fit naturally into the data system, while others will have to put in extra work to make themselves fit, and others will have to modify themselves or misrepresent themselves to fit into the system.

So, for example, if we made a form that someone needed to enter their address, we could assume everyone is in the United States and not have any country selection.
- Address fields:
  - Street address
  - City
  - State
  - Zip Code

Someone in another country would have to try to find a way to indicate that they aren't in the United States even though there is no clear place to indicate that. If this is a form for shipping to people in the US only, then this limitation might make sense.

If we wanted people to be able to enter other countries we could make a country drop-down tool to select a country, but then would we auto-fill it with a country? If there is a list of countries to scroll through, what order do we put them in? If it's alphabetical, that will make it easier for people in countries whose name starts with "A."


## Form fails
Let's look at some examples where forms show problems with data entry and representation:

### Name Length
Here are some screenshots from a [help forum discussion](https://ttlc.intuit.com/community/taxes/discussion/my-last-name-is-to-long-what-do-i-do/00/655670) {cite:p}`MyLastName2019` on the United States tax software TurboTax:

![Screenshot from turbotax help forum. A user in 2019 posted the question: "My last name is too long, what do I do?"](tax_name1.png)

![Screenshot from turbotax help forum. A user in 2019 replied "You can fix that by removing the last letters that don't fit. The IRS matches the social security number with only the first few letters of the last name."](tax_name2.png)

![Screenshot from turbotax help forum. A user in 2020 replied "Same thing for me. I end up filling by mail because it fails every time."](tax_name3.png)

As you can see, TurboTax has a limit on how long last names are allowed to be, and people with too long of names have different strategies with how to deal with not fitting in the system.

### Gender
Data collection and storage can go wrong in other ways as well, with incorrect or erroneous options. Here are some screenshots from a thread of people collecting strange gender selection forms:

- [![Tweet from user "Coding Drag Queen Anna Lytical" with handle "@theannalytical". The tweet text is "send me the worst gender selection forms you've seen, I'll start" and the image is of a dropdown with the following options: Female, Male, N/A, Unknown, Tax Entity"](gender_select1.png)](https://twitter.com/theannalytical/status/1349392166716657664?s=20) {cite:p}`annalytical[@theannalytical]SendMeWorst2021`

- [![image that says "ah yes, the three genders" and below it is a screenshot of a form that says "What is your gender? Please select one." and the options are: "Male", "Female", and "I have no plans to purchase a new vehicle"](gender_select2.png)](https://twitter.com/annabookwriter/status/1349410399574102016?s=20) {cite:p}`annaholmes[@annabookwriter]TheannalyticalMckellogsNot2021`

You can see more of these types of forms at [https://genders.wtf/](https://genders.wtf/)

% TODO: Add Individual vs. systemic analysis here, include [structural problem tweet](https://twitter.com/athertonkd/status/1120376944061583360) {cite:p}`kelseyd.atherton[@athertonkd]OhYouRe2019`

## Learn more
### Systemic Power
- Systems have power to “bestow humanity on marginalized others” (Professor Anna Lauren Hoffmann)
  - Blog Post: [Data Violence and How Bad Engineering Choices Can Damage Society](https://medium.com/s/story/data-violence-and-how-bad-engineering-choices-can-damage-society-39e44150e1d4) {cite:p}`hoffmannDataViolenceHow2018`
  - Video: [What We Really Talk About When We Talk About Ethics: Navigating History, Privilege, and Power in Information and Data Science](https://vimeo.com/250857851) {cite:p}`academiesWhatWeReally2018`
  - Video: [Beyond Fairness: Discourse, Violence, and Justice in a Datafied World](https://vimeo.com/335550401) {cite:p}`designusebuildAnnaLaurenHoffmann2019`

### [Design Justice](https://design-justice.pubpub.org/) {cite:p}`DesignJustice`
- “Design justice is a framework for analysis of how design distributes benefits and burdens between various groups of people. Design justice focuses explicitly on the ways that design reproduces and/or challenges the matrix of domination (white supremacy, heteropatriarchy, capitalism, ableism, settler colonialism, and other forms of structural inequality).”
- It’s also about which groups get to be part of the design process itself.
- [![Photo of Sasha Costanza-Chock](costanza-chock.png)](https://en.wikipedia.org/wiki/Sasha_Costanza-Chock) [Sasha Costanza-Chock](https://en.wikipedia.org/wiki/Sasha_Costanza-Chock) {cite:p}`SashaCostanzaChock2023`, present USA