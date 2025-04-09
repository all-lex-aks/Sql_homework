create table if not exists Tracks (
TrackID serial primary key,
 
);

create table if not exists Albums (
AlbumID serial primary key,
 
);

create table if not exists Performers (
PerformerID serial primary key,
 
);

create table if not exists Albums_Performers (
ID serial primary key,
 
);

create table if not exists Genres (
GenresID serial primary key,
 
);

create table if not exists Performers_Genres (
ID serial primary key,
 
);

create table if not exists Collections (
CollectionID serial primary key,
 
);

create table if not exists Tracks_Collections (
ID serial primary key,
 
);
