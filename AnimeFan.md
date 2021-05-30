# AnimeFan (◕‿◕)

You will use the [Jikan API](https://jikan.moe/) to build an Anime collection app that lets users explore top Anime titles and add them to their watchlist.

## Stage 1

### Design

The design: <https://www.figma.com/file/Rai0GbWXaH9fK1KN4bE6g8/AnimeFan?node-id=0%3A1>

You will implement a responsive layout and provide a smooth experience to both desktop and mobile users. The design has differences in certain screen sizes but represents the same dataset and has the same functionality.

- Primary color: `#EB5757`
- Text and bullet color `#31353F`
- Text color for card subtitles `#31353fcc`
- Header font `Sedgwick Ave` 
- Body font `Roboto`
- Use the Material Icon font
- Use [this image](https://www.pngix.com/pngfile/big/236-2366727_one-piece-png-wanted-monkey-d-luffy-transparent.png) for the header.
- The header and the navigation bars (top/bottom) _don't_ scroll with the document.

### Specs

#### Screens

- The app has two screens, **All Titles** and **Watchlist**, displayed as tabs. The app starts with **All Titles** as the active screen.
  - Desktop: The tabs are displayed as top tabs.
  - Mobile: The tabs are displayed as bottom tabs.
- Clicking **Watchlist** changes the active view to the **Watchlist** screen and the **Watchlist** tab is highlighted.
  - If the user hasn't added any titles to their watchlist yet, the **Watchlist** screen displays a view informing the user that titles added to the list will be displayed here.
  - If the user adds at least one title to their list, the **Watchlist** screen shows anime title cards and the tab also displays a number in parentheses, indicating the number of titles in the list.
- Clicking **All Titles** changes the active view back to the **AllTitles** screen and the **All Titles** tab is highlighted.
- The app fetches the data only when first launched and the tabs are displayed properly while fetching. During fetching:
  - The **All Titles** screen displays a loading spinner instead of cards.
  - The **Watchlist** tab is disabled. Clicking on it has no effect.

#### Anime titles

- Available titles are displayed as cards.
- Only titles that have been shown on TV are displayed. The rest are omitted.
- The title's rating is in a scale of 0 to 5.
- If end date is missing, write **present** instead.
- If episodes are missing, omit the field.
- All cards have a **watchlist action button**.
  - If the title _is not_ in the user's list:
    - The button has a **plus icon** and says **Watchlist**.
    - Clicking the button adds the Anime title to the user's watchlist.
    - Hovering over the button shows a tooltip text that reads **Add to watchlist**.
  - If the title is in the user's list:
    - The button has a **check-mark icon** and says **Added**.
    - Clicking the button removes the title from the list
    - Hovering over the button shows a tooltip that reads **Remove from watchlist**.

### Technical Guidelines for React

- Write the app in TypeScript and React.
- Use only function components and hooks.
- Use the fetch API to get your data. Use async/await.
- Don't use react router or other routing libraries and don't bother with browser history for now.
- Test your functions using jest. Don't test your components for now.
- Write your styles using either SCSS and BEM methodology or Styled Components/Emotion.
- An important part of this stage is to figure out how to hold the Anime titles that the user has added to their watchlist.

Use the following endpoint to fetch data about the top 50 Anime titles: `https://api.jikan.moe/v3/top/anime/1`

Explore the response to determine how to satisfy the provided specs.

#### Takeaways

- React hooks
- Deriving data and producing viewmodels
- Conditional rendering
- Fetch API
- Working with JSON payloads
- async/await

## Stage 2

- Deploy on github pages
- ci

## Stage 3

- Runtime validation
- Remember selections
- Add a Filter dropdown
- Add an AnimeTitleDetails screen
- Add a search bar
- Specify year and season
- Dark theme
