# Pangolin Localization Community Event

## Pangolin Localization Community Event

As the Pangolin community continues to grow, we are welcoming new users from all over the world. To make sure that our website is as international as our user base, we are organizing an event to source translations from the community.

The event will run for a week, from 06/14/2021 00:00 UTC to 06/24/2021 00:00 UTC

The target languages for this event are: **Chinese \(Mandarin\), French, German, Japanese, Spanish & Turkish** but more languages might be added in the future, so stay tuned!

### Prizes

* 100 PNG for the best submission in each language \(Chinese \(Mandarin\), French, German, Japanese, Spanish, Turkish\)
* 50 PNG for the runner up in each language

### Rules

1. Only one submission per user \(you can not submit in different languages\).
2. If two or more submissions are found to be exactly identical, all will be disqualified.
3. Selection of the winners will be done by speakers of each language from the Pangolin team
4. Criteria include accuracy, understandability and how well the translation fit into the current website's interface. 
5. To be valid, translations must be submitted as a pull request to the Pangolin community repository \(see instructions below\).

### Instructions

The files to be translated are the json files located in the `public/locales/` [folder](https://github.com/pangolin-community/interface/blob/localization/public/locales) of the interface repository of the [Pangolin community Github.](https://github.com/pangolin-community) Select the file corresponding to the language you will translate to:

| Filename | Language |
| :--- | :--- |
| de.json | German |
| es.json | Spanish |
| fr.json | French |
| jp.json | Japanese |
| tr.json | Turkish |
| zh-cn.json | Chinese \(Mandarin\) |

Note that you only need to translate the values \(the part on the right\) of the JSON, not the keys \(the part on the left, before the colon\)!

For instance a translation of

```text
{
  "header": {
    "swap": "Swap",
    "pool": "Pool",
    "vote": "Vote",
    ...
```

Would look like this:

```text
{
  "header": {
    "swap": "スワップ",
    "pool": "プール",
    "vote": "投票",
    ...
```

Once you have translated all the values in the JSON file, you can follow the steps below to submit your translation as a pull request on Github:

1. Create a Github account
2. Go to [https://github.com/pangolin-community/interface/blob/master/public/locales](https://github.com/pangolin-community/interface/blob/master/public/locales) and select the file you have translated.
3. In the screen that shows up, click on the Pencil icon to **Edit the file in your fork of this project**: 
4. A new window will open with an editor. You can use it replace the content of the file with that of your translation.
5. When you are done, navigate to the bottom of the page. If your email is not public in your Github profile or you would like to be contacted some other way if you were to win, you can tell us how to contact you in the **Add an optional extended description...** field. Feel free to add other comments if you need to.
6. Once everything is ready click on **Propose changes**: ![](proposechanges.jpg)
7. You will be taken to a new page to let you review your changes. Make sure that the base repository \(underlined in red below\) is set to `pangolin-community/interface`, check that your changes are good to go and click on **Create pull request** when you're ready to submit. ![](pullrequest.jpg)
8. You will be taken to a new page, just click **Create pull request** again. ![](pullrequest2.jpg)
9. And you're good to go! Thank you for your submission!

### Tips

1. Try to keep user interface constraints in mind when translating. For instance if you translate a 5 letter English word as a 50 letter long expression in your language, the translated expression might not be fully displayed on the site's interface.
2. Stay consistent, avoid translating the same key terms \(swap, pool, token...\) differently unless context really calls for it.
3. Do not translate variables. Variables sometimes appear between curly brackets in the locale file. For instance, in the following string: `"The token list \" {{oldList}} \" has been updated to "`, `{{oldList}}` is a variable that will display the name of the updated list. You may change its position in the sentence, but do not translate the name of the variable.
4. Try running the site locally on your computer with your locale before submitting to see how it looks like. Instructions to run the site locally are available in the [repository's README](https://github.com/pangolin-community/interface/).

