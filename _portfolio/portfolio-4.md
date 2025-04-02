---
title: "Spotify Playlist Analyzer"
excerpt: "Built an API-based application to extract and sort all music genres from a user's Spotify library using Terraform, AWS, and Python<br/><img src='/images/spotify-world.png'>"
collection: portfolio
---

*Personal*

How can you take your "taste profile" with you to another music platform? This is the problem I set to out to solve with Spotify Playlist Analyzer. I had all my music in Spotify, which together constituted a taste profile. Without such a profile, I couldn't easily move to other music platforms as it would take too long to discover new music and build a library.

So, I built Spotify Playlist Analyzer to provide an easy solution to this problem. The user puts all of his liked songs into one large playlist, makes it public, hits the API with the URL of the playlist, and the Analyzer returns a list of genres sorted by frequency. I used AWS Elastic Container Service to host the application, Jenkins for CI, and Poetry for the Python project. All cloud infrastructure is Infrastructure-as-Code deployed via Terraform.

[🦊](https://gitlab.com/homelab.cloud/spotify-playlist-analyzer)

