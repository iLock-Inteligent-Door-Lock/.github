<h1 align="center">Hello everyone </h1>
name: Dynamic Hello

on:
  push:
    branches:
      - main

jobs:
  build:
    runs-on: ubuntu-latest

    steps:
      - name: Checkout repository
        uses: actions/checkout@v2

      - name: Set up Hello
        run: echo "hello: 'Hello, world!'" >> $GITHUB_ENV

      - name: Replace {{ hello }} in README
        run: |
          sed -i "s/{{ hello }}/$HELLO/g" README.md

      - name: Commit and push changes
        run: |
          git config --local user.email "action@github.com"
          git config --local user.name "GitHub Action"
          git add README.md
          git commit -m "Update README with dynamic hello"
          git push

<p align="center">
  <img src="https://github.com/iLock-Inteligent-Door-Lock/iLock-Inteligent-Door-Lock/blob/main/obraz_2023-07-19_210359785.png">
</p>

<h1 align="center"> This project is creating by two Automation and Robotics students </h1>

 - [Bartosz Leśniak](https://github.com/BartoszLesniak333)
 - [Michał Łazarz](https://github.com/miq312)

<h1 align="center">About a project </h1>
