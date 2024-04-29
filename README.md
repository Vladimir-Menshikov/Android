## 1. A 'Unit/Currency Converter' application.

1. 3 different unit categories (distance, weight, currency)
2. 3 different units in each category.
3. Calculator-like num pad and two fields for original and converted values.
4. A keyboard and data are in separate android fragments.
   - portrait orientation: fragments are placed in a row (keyboard below data fragment)
   - landscape orientation: fragments have to be aligned in line.
5. A 'premium' build flavour.
   - A button, that will switch initial and converted values (and units) and vice-versa.
   - A button to copy current value to the clipboard near each data field.
   - Source sets to define different layouts and files with code for each flavour.

## 2. A 'Tabata timer' application.
([Reference](https://play.google.com/store/apps/details?id=com.evgeniysharafan.tabatatimer&hl=ru))

1. A user can create different timer sequences and switch between them.
2. Home page - a list of sequences
   - CRUD for them
3. Sequence properties:
   - title
   - colour
4. Timer page:
   - remaining time of the current phase
   - list of upcoming phases
   - controls to pause, go back and forth through the sequence or to leave this page and cancel the timer
5. Edit page:
   - tweak duration of each phase (workout, rest, warm-up, cooldown)
   - change number of phase repetitions and rest periods between them
   - define sequence properties
6. While running, each phase switch triggers a sound to warn user.
7. The timer doesn't stop when user leaves the app.
8. Settings page (implemented with AndroidX Preference library):
   - day / night theme
   - change app font size (without app reload)
   - a button to clear all stored data
   - switch app locale (a choice between two languages at least).
9. Application has a splash screen with app name or artwork to entertain the user while the app is being loaded.

## 3. Online  'Battleship' game.

1. Two players are able to participate in the game from different devices.
2. Firebase Firestore as a back-end.
3. Authentication using any auth provider (Google, Facebook) or plain email-password pair.
4. User 1 creates a game and shares generated game ID with opponent.
5. Opponent (user 2) joins the game via given ID.
6. User 1 device acts as a server and is responsible for game state updates.
7. User 2 device subscribes to state changes in DB and updates interface.
8. User statistics page with previous games
9. User profile page:
    - nickname change
    - avatar (user can switch between these two options in profile)
      - remote storage using Firebase File storage
      - [Gravatar](https://ru.gravatar.com/)
