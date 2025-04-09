create table if not exists Tracks (
TrackID serial primary key,
Title varchar(80) not null,
Duration integer not null,
AlbumID integer not null references Albums(AlbumID)
);

create table if not exists Albums (
AlbumID serial primary key,
Title varchar(80) not null,
Year_of_release integer not null
);

create table if not exists Performers (
PerformerID serial primary key,
Nickname varchar(80) not null
);

create table if not exists Albums_Performers (
ID serial primary key,
AlbumID integer not null references Albums(AlbumID),
PerformerID integer not null references Performers(PerformerID)
);

create table if not exists Genres (
GenreID serial primary key,
Genre_name varchar(80) not null
);

create table if not exists Performers_Genres (
ID serial primary key,
PerformerID integer not null references Performers(PerformerID),
GenreID integer not null references Genres(GenreID)
);

create table if not exists Collections (
CollectionID serial primary key,
Title varchar(80) not null,
Year_of_release integer not null 
);

create table if not exists Tracks_Collections (
ID serial primary key,
TrackID integer not null references Tracks(TrackID),
CollectionID integer not null references Collections(CollectionID)
);
