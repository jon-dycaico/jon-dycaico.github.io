---
title: "Spotify Playlist Analyzer"
excerpt: "Built an API-based application to extract and sort all music genres from a user's Spotify library using Terraform, AWS, and Python<br/><img src='/images/spotify-world.png'>"
collection: portfolio
---

When the platform owns your taste profile, how can you take it with you?

This is the problem I set to out to solve with Spotify Playlist Analyzer (SPA). I had all my music in Spotify, which together constituted a "taste profile". Without such a profile, I could not easily move to other music platforms as it would take too long to discover new music and build a library.

Thus, I built SPA to provide an easy solution to this problem. The user puts all of his liked songs into one large playlist, makes it public, hits the API with the URL of the playlist, and the Analyzer returns a list of genres sorted by frequency. I ended up using ECS to host the application, Jenkins for CI, and Poetry for the Python project. All infrastructure is IaC deployed via Terraform.

