# Ukraine Develorers Network

   The social network and Google news portal built on React/Redux architecture.

[![Review](https://user-images.githubusercontent.com/40334272/85372438-8312cf00-b53a-11ea-885f-b994aba5a635.jpg)](https://www.youtube.com/watch?v=wipq1YQxvFU)
[![Review](https://github.com/user-attachments/assets/701d2bbb-7402-406a-be98-9c3c97afde98)](https://www.youtube.com/watch?v=wipq1YQxvFU)

   When I was a child, I dreamed of creating my own social network. This project is a step toward that childhood goal) I would be grateful for any feedback or suggestions to improve the code.

[![Review](https://github.com/user-attachments/assets/08222949-cb5a-40ac-adf8-66feb463b641)](https://www.youtube.com/watch?v=wipq1YQxvFU)

## 📂 Folder structure

 ```
src
   ├── api               /* side effects, requests
   └── assets            /* images, fonts, additional files
   |     ├── fonts
   |     ├── audio
   |     └── image
   └── components
   |     └── common      /* reusable components
   |      ...
   |     ├── Login       /* main components, routes structure
   |     ├── Profile
   |     ├── Dialogs
   |     ├── Users
   |     ├── News
   |     ├── Settings
   |     └── NotFound
   ├── hoc               /* higher order components
   ├── redux             /* reducers, actions, action creator, thunks
   ├── scss              /* global styles, mixins, vars
   ├── selectors         /* selectors
   └── utils             /* handlers, validation, other...

```
 ## 💻 Technology stack
- ### Architecture
     - **UI**(React), **BLL**(Redux), **DAL**(Axios, Thunk)

- ### Build system & environment
   - The project was created using Create React App (CRA). Part of the application is written with class components, some parts have been rewritten using hooks.

- ### Design
   - I designed the UI myself, drawing inspiration from Behance, Apple, and Facebook. The style is a mix of minimalism, metro, and flat design, with some elements of skeuomorphism.

- ### Layout and styling
   * **Styling**. Used:
     * **css modules** - solves the problem of global scope.
     * **sass(scss)** - for using variables, mixins, and nesting.
     * **BEМ** - In this case, since some of its responsibilities are handled by modules, it allows SCSS to be expanded and makes it convenient to create nested structures and split a component into sub-blocks.
     * for scrollbar customization, I used **react-perfect-scrollbar**.
     * for convenient class name combinations, I integrated the **classnames**.
     * for styling the select element, I used **react-select**.
   - **Grid**. I based the layout on **flex**, and used grid in some areas. I decided not to use Bootstrap or Materialize, as even with these frameworks, pre-built components need to be transformed and overridden with custom styles. Additionally, building the grid with flex doesn’t take much time.
   - **Responsive design**: I used the standard responsive approach, with flexible and adaptive layout. To prevent rendering unused components based on screen width, I used the **react-responsive library**(which monitors resize and innerWidth).
   - **Animations**. I wrote all animations manually without using any libraries. To link transition animations with the component lifecycle, I used the **react-transition-group** library in some places.

- ### Store
   - For managing the global state of the application, I initially wrote a simplified version of Redux to understand its structure and the problems it solves. Later, I used **redux, react-redux**  to conveniently integrate Redux with React (using connect).

- ### Routing
   - For routing implementation, I used the **react-router-dom library**.

- ### API
   - For working with REST APIs, I used the **axios library**. To enable the creation of asynchronous actions and side effects, I integrated **redux-thunk**.

- ### Forms
   - I integrated redux-form, but I didn’t like how it creates its own branch in the global Redux store. I believe that data should be handled at the local level. As a result, some parts were written without using the library.

- ### Selectors
   - For caching selectors, I used react-select.

 ## 💻 Structure and functionality

 - ### **Header panel**
   - *Displaying authorized user data (Username/Photo).*
   - *LogIn/LogOut based on authentication with redirection to the login page.*

- ### **Login page**
   - *The form for entering authentication credentials (username/password) with client-side and server-side validation.*
   - *CAPTCHA with a refresh button (activates after more than 4 incorrect password attempts).*
   - *Redirection to the profile upon successful login, and redirection from other pages if the user is not authenticated.*

- ### **Profile page**
   - **User info**
     - *Mode switch (authenticated user/viewing user profiles)*
     - *Displaying and changing the user's main profile photo.*
     - *Displaying and editing the status.*
     - *Displaying user data: About, Looking for a job, Website, and Contacts (Facebook, Twitter, Instagram, GitHub, Website).*
     - *Profile edit button with redirection to the settings page/message sending button if the profile is in view mode.*
   - **Posts**
     - *Creating and deleting posts (changes are currently stored locally).*

- ### **Dialogs page**
   - *Lists of dialogs and messages (updated every 15 seconds).*
   - *Message sending form with validation.*
   - *Functionality for switching between active dialogs.*
   - *Functionality for sending and receiving messages.*
   - *Displaying the number of new messages for each dialog.*

- ### **Users page**
   - *User list.*
   - *Changing the number of users on the page.*
   - *Pagination.*
   - *Subscribe/Unsubscribe from a user.*
   - *Creating a dialog with a user.*
   - *Viewing the profile of the selected user.*

- ### **News portal**
   - *News feed.*
   - *Changing the number of news items on the page.*
   - *Category selection.*
   - *Pagination.*
   - *Number of search results.*
   - *Change of layout (tablet/list/large).*

 - ### **Settings page**
   - *Changing the user's photo, name, status, active search status, description, detailed description, and contacts.*

 - ### **Sidebars**
   - *Navigation panel.*
   - *Active dialogs panel with auto-refresh.*
   - *Latest news panel with auto-refresh.*
   - *Panel displaying the number of registered users/app version.*
   - *Background audio player with Play/Pause state toggle.*

 - ### **Notifications**
   - *Displaying the waiting status for a server response.*
   - *Notifications display system.*
   - *Error handling.*

## 📱 Authentication, API keys
  -  The application includes default API keys for testing. You can use them, but they have a limited number of requests.
  -  You can generate new keys here and set them in api.js:
      - [Google News API](https://newsapi.org/s/google-news-api)
      - [Social Network API](https://social-network.samuraijs.com/) (also you can register a new user)

## 🚀 Run the application locally in 5 minutes.
Google News doesn't work due to CORS restrictions. If you want to test it, you must download and run the application on localhost. Sometimes, errors may occur due to server overload.
You can run the application in your local development environment in 5 minutes by following these steps:
1. **Install Node.js(v14)** [download](https://nodejs.org/en/).
2. **Install Yarn** [download](https://classic.yarnpkg.com/en/docs/install#windows-stable).
3. **Download my repository** .
4. **Install dependencies** .

   Open the CLI in the application folder and set it up with a single command.:

   ```shell
   yarn install

   ```
5. **Start aplication** .

   Set it up with a single command in the CLI:

   ```shell
   yarn start

   ```
 ## 📱 It needs to be improved.
  -  Replace redux-form with Formik.
  -  Write backend part, as Google News only works locally, and the main server is very slow and often cannot handle the load.

 ## 📷 Screenshots
![1](https://user-images.githubusercontent.com/40334272/85372502-9e7dda00-b53a-11ea-9796-f6191a5720a8.png)
![2](https://user-images.githubusercontent.com/40334272/85372520-a5a4e800-b53a-11ea-91ef-7f6d793e2e4b.png)
![3](https://user-images.githubusercontent.com/40334272/85372523-a6d61500-b53a-11ea-9866-ca9dff8ddd0d.png)
![4](https://user-images.githubusercontent.com/40334272/85372525-a6d61500-b53a-11ea-9baa-35daeb9e7bda.png)
![5](https://user-images.githubusercontent.com/40334272/85372527-a76eab80-b53a-11ea-828f-cda6815c7468.png)
![6](https://user-images.githubusercontent.com/40334272/85372531-a76eab80-b53a-11ea-840a-c1fb28fe4d3d.png)

 ## 🚀 Quality assurance
![1](https://github.com/user-attachments/assets/6c85a1e1-6e49-4ec8-b1c0-451473c381c3)
![1](https://github.com/user-attachments/assets/83200c98-e43e-474a-9f28-7cc0d3f824dc)
![1](https://github.com/user-attachments/assets/0a7536ab-9733-44dc-b005-f74de73cb339)
