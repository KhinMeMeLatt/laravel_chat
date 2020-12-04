## Laravel chat application

This application is implemented by using pusher API.

## Screenshot
![Chat Screenshot](https://github.com/KhinMeMeLatt/laravel_chat/blob/main/chat_screenshot.JPG)

## Installation

### Step 1: Clone this repo

```bash
git clone git@github.com:KhinMeMeLatt/laravel_chat.git
cd laravel_chat
```

### Step 2: Install composer

```bash
$ composer install
```

### Step 3: Create and setup .env file

```bash
make a copy of .env.example and rename to .env
$ php artisan key:generate
put database credentials in .env file
```

### Step 4: Migrate and insert records

```bash
$ php artisan migrate
$ php artisan tinker
$ factory(App\User::class, 30)->create();
$ factory(App\Message::class, 500)->create();
```

### Create and setup pusher account
- log in to [pusher](https://pusher.com/) and create new app
- put pusher credentials to .env file

```bash
PUSHER_APP_ID=YOUR_PUSHER_APP_ID
PUSHER_APP_KEY=YOUR_PUSHER_APP_KEY
PUSHER_APP_SECRET=YOUR_PUSHER_APP_SECRET
PUSHER_APP_CLUSTER=YOUR_PUSHER_APP_CLUSTER
```

- replace PUSHER_APP_KEY in your app.blade.php

```bash
var pusher = new Pusher('a4a3daee72b47957427b', {
                 cluster: 'mt1',
                 forceTLS: true
});
```
## Acknowledgement
-   **code for you** - [Laravel realtime chatting application with php laravel 5.8 using pusher](https://www.youtube.com/watch?v=cPGhs94Rj5E)
