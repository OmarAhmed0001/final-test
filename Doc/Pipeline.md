## Pipeline
# first install AWS dependencies using the following steps in circleci
- run:
          name: Install pip
          command: |
            sudo apt update
            sudo apt install -y python3-pip python-dev
      - run:
          name: Install AWS dependencies
          command: |
            sudo pip3 install awsebcli
            
# second install dependencies in the frontend app using the following steps in circleci

      # Use root level package.json to install dependencies in the frontend app
      - run:
          name: Install Front-End Dependencies
          command: |
            echo "NODE --version"
            echo $(node --version)
            echo "NPM --version"
            echo $(npm --version)
            npm run frontend:install

# third install dependencies in the backend API using the following steps in circleci

      # TODO: Install dependencies in the the backend API
      - run:
          name: Install API Dependencies
          command: |
            echo "TODO: Install dependencies in the the backend API  "
            npm run api:install

# fourth Lint the frontend using the following steps in circleci

      # TODO: Lint the frontend
      - run:
          name: Front-End Lint
          command: |
            echo "TODO: Lint the frontend"
            npm run frontend:lint

# fifth Build the frontend app using the following steps in circleci

      # TODO: Build the frontend app
      - run:
          name: Front-End Build
          command: |
            echo "TODO: Build the frontend app"
            npm run frontend:build

# sixth Build the backend API using the following steps in circleci

      # TODO: Build the backend API
      - run:
          name: API Build
          command: |
            echo "TODO: Build the backend API"
            npm run api:build

# seventh deploy the backend API and The frontend app using the following steps in circleci

    # deploy step will run only after manual approval
      - run:
          name: Deploy App
          # TODO: Install, build, deploy in both apps
          command: |
            echo "# TODO: Install, build, deploy in both apps"
            npm run api:deploy
            npm run frontend:deploy
  