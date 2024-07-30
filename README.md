# Spotify Playlist Creation using Terraform

![Screenshot_2024-07-30_17_13_24](https://github.com/user-attachments/assets/3859fd77-0b13-41b6-b97d-2cd9b4c79599)
![Screenshot_2024-07-30_17_13_54](https://github.com/user-attachments/assets/fea41c73-7635-4b39-bda2-86eb0dc82c4b)


This project automates the creation of Spotify playlists using Terraform.

## Table of Contents
- [Introduction](#introduction)
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Configuration](#configuration)
- [Usage](#usage)
- [License](#license)

## Introduction
This project demonstrates how to use Terraform to create and manage Spotify playlists programmatically. Terraform is an open-source infrastructure as code software tool that provides a consistent CLI workflow to manage hundreds of cloud services.

## Prerequisites
Before you begin, ensure you have met the following requirements:
- You have a Spotify account.
- You have `terraform` installed on your local machine. [Install Terraform](https://learn.hashicorp.com/tutorials/terraform/install-cli)
- You have a Spotify Developer Application set up. [Create a Spotify Developer Application](https://developer.spotify.com/dashboard/applications)
- You have Docker installed if you are using a Docker container to run Terraform. [Install Docker](https://docs.docker.com/get-docker/)

## Installation
1. Clone this repository:
    ```sh
    git clone https://github.com/BlAcKyCoDe50/spotify-terraform.git
    cd spotify-terraform
    ```

2. Install the required Terraform providers:
    ```sh
    terraform init
    ```

## Configuration
1. Create a `.env` file in the root directory of the project and add your Spotify credentials:
    ```sh
    SPOTIFY_CLIENT_ID=your_spotify_client_id
    SPOTIFY_CLIENT_SECRET=your_spotify_client_secret
    SPOTIFY_REDIRECT_URI=your_spotify_redirect_uri
    ```

2. Update the `terraform.tfvars` file with the necessary variables:
    ```hcl
    playlist_name = "My Terraform Playlist"
    playlist_description = "A playlist created with Terraform"
    tracks = [
        "spotify:track:track_id_1",
        "spotify:track:track_id_2",
        "spotify:track:track_id_3"
    ]
    ```

## Usage
1. Authenticate with Spotify:
    ```sh
    terraform apply
    ```

2. Follow the instructions in the terminal to authenticate with Spotify. This will open a browser window where you need to log in to your Spotify account and authorize the application.

3. After successful authentication, Terraform will create the playlist with the specified tracks.


## Contributing
If you would like to contribute to this project, please open an issue or submit a pull request.

## Acknowledgements
- [Spotify Web API](https://developer.spotify.com/documentation/web-api/)
- [Terraform](https://www.terraform.io/)
- [Terraform Spotify Provider](https://registry.terraform.io/providers/conradludgate/spotify/0.2.7)
- [Full Guide step by step](https://cloudchamp.notion.site/Creating-Multiple-Spotify-Playlists-Using-Terraform-3171668ad3074aa8acab147ad85e26f8)
