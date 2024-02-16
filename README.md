# TweetDiary
A secure, tweet diary app using Firebase for private reflection and concise expression.

# Key Features and Considerations

## Authentication and Allow-List:

* Integrate Firebase Authentication for Google Sign-in using appropriate plugins and follow best practices for secure handling of user credentials.
* Implement a mechanism to verify users against an allow-list stored securely, either locally within the app or remotely on a server (consider security implications of each approach).
* Display appropriate messages or redirect users if they're not on the allow-list.

## Tweet Input and Validation:

* Create a text field with character count, allowing up to 280 characters.
* Use regular expressions or other validation methods to ensure tweets adhere to Twitter's requirements (https://help.twitter.com/en/rules-and-policies/twitter-rules).
* Consider using packages like tweet_composer or twitarr for advanced tweet composition features.

## Firebase Database:

* Set up a Realtime Database or Firestore instance in your Firebase project.
* Store tweets as objects with properties like text, timestamp, userId, etc., considering data schema design for efficiency and queryability.
* Implement appropriate security rules to restrict access and modification of tweet data.
* Adhere to Firebase security best practices to protect user data and prevent unauthorized access or modification.


## Tweet Listing and Load More:

* Use widgets like ListView or PaginatedListView to display the past 200 tweets in descending order (newest first).
* Fetch tweets in batches from the database as the user scrolls up, using pagination techniques to efficiently load more data.
* Consider using a state management solution like Provider or MobX to manage tweet data and loading state effectively.

## Search Functionality:

* Implement a search bar that filters the locally loaded tweets based on user input, using TextField or CupertinoTextField and building custom filtering logic.
* Provide clear search results, highlighting matched keywords or indicating no results found.

## Chat-Room Style Presentation:

* Design the tweet listing component with appropriate styling and layout, aiming for a chat-room or message-like appearance.
* Consider using packages like chat_bubbles or bubble for pre-built chat UI elements.

## Testing and Documentation

* Authentication, allow-list verification, tweet validation, and database interactions.
* Handle potential edge cases and error scenarios gracefully, providing informative messages to the user.
* Clearly document your implementation choices and reasoning for future reference and maintainability.
