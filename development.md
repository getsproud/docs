## Improvements

#### services

Edit dockerfiles of nodejs services to run nodemon and build on the fly inside the container.
Skaffold should sync the files like in the app services and don't rebuild the container everytime a file changes.
This speeds up the dev process a lot.
