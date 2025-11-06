# Entity Relationship Diagram

Reference the Creating an Entity Relationship Diagram final project guide in the course portal for more information about how to complete this deliverable.

## Create the List of Tables

users: id, username, email, avatar_url, bio, created_at

games: id, title, slug, release_date, summary, cover_url, avg_rating, created_at

genres: id, name

platforms: id, name

developers: id, name

Junctions

game_genre: (game_id, genre_id) PK composite

game_platform: (game_id, platform_id) PK composite

game_developer: (game_id, developer_id) PK composite

User activity (signals for recs)

user_game: id, user_id FK, game_id FK, status{playing|completed|on_hold|dropped|wishlist}, rating(0–10), liked bool, hours, notes, completed_at, created_at, updated_at, UNIQUE(user_id,game_id)

Reviews & social

reviews: id, user_id FK, game_id FK, title, body, rating, created_at, updated_at

review_comment: id, review_id FK, user_id FK, body, created_at

follows: follower_id FK, followee_id FK, created_at (PK (follower_id, followee_id))


## Add the Entity Relationship Diagram

<img width="907" height="1490" alt="gamilist_erd" src="https://github.com/user-attachments/assets/1f3359f2-5469-4619-81cf-71e6908e87ab" />
