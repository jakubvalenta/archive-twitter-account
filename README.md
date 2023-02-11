# Twitter Archive

A script to archive a public Twitter profile. It downloads all tweets as one
[JSON Lines](https://jsonlines.org/) file and all photos as JPEGs or PNGs.

It uses [twarc](https://twarc-project.readthedocs.io/en/latest/) under the hood.

## Prerequisites

You will need to [sign up for a Twitter developer
account](https://developer.twitter.com/en/docs/twitter-api/getting-started/getting-access-to-the-twitter-api),
create a Project and an App, and get your App's key and tokens.

## Installation

1. Install Python 3.

    On Mac:

    ```shell
    $ brew install python3
    ```

    On Arch Linux:

    ```shell
    # pacman -S python
    ```

2. Install Twitter Archive's dependencies:

    ```shell
    $ python -r requirements.txt
    ```

## Usage

1. Get your Twitter App's bearer token (it should be somewhere
   [here](https://developer.twitter.com/en/portal/projects-and-apps)) and export
   it as an environment variable:

    ```shell
    $  export BEARER_TOKEN='<your twitter app bearer token>'
    ```

2. Call Twitter Archive with the username of the account you'd like to archive.
   Example:

     ```shell
     $ ./twitter-archive TwitterDev
     ```

3. Done. You can now find the downloaded data in the `./data` directory.
   Example:

    ```
    data
    └── TwitterDev
        ├── media
        │   ├── Ffbx1jMXoAEU7Fh.jpg
        │   ├── ...
        │   └── FevXHTtXoAAoGyu.jpg
        ├── media_objects.jsonl
        └── timeline.jsonl
    ```

## Contributing

__Feel free to remix this project__ under the terms of the [Apache License,
Version 2.0](http://www.apache.org/licenses/LICENSE-2.0).
