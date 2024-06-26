-- Create database
CREATE DATABASE NBAStats;
USE NBAStats;

-- Table: Players
CREATE TABLE Players (
    PlayerID INT PRIMARY KEY,
    FirstName VARCHAR(50),
    LastName VARCHAR(50),
    TeamID INT,
    Position VARCHAR(10),
    Height FLOAT,
    Weight FLOAT,
    BirthDate DATE,
    CONSTRAINT fk_team FOREIGN KEY (TeamID) REFERENCES Teams(TeamID)
);

-- Table: Teams
CREATE TABLE Teams (
    TeamID INT PRIMARY KEY,
    TeamName VARCHAR(50),
    Conference VARCHAR(20),
    Division VARCHAR(20)
);

-- Table: Games
CREATE TABLE Games (
    GameID INT PRIMARY KEY,
    Date DATE,
    HomeTeamID INT,
    AwayTeamID INT,
    HomeTeamScore INT,
    AwayTeamScore INT,
    CONSTRAINT fk_home_team FOREIGN KEY (HomeTeamID) REFERENCES Teams(TeamID),
    CONSTRAINT fk_away_team FOREIGN KEY (AwayTeamID) REFERENCES Teams(TeamID)
);

-- Table: PlayerStats
CREATE TABLE PlayerStats (
    PlayerID INT,
    GameID INT,
    Points INT,
    Assists INT,
    Rebounds INT,
    Steals INT,
    Blocks INT,
    MinutesPlayed INT,
    CONSTRAINT pk_player_stats PRIMARY KEY (PlayerID, GameID),
    CONSTRAINT fk_player FOREIGN KEY (PlayerID) REFERENCES Players(PlayerID),
    CONSTRAINT fk_game FOREIGN KEY (GameID) REFERENCES Games(GameID)
);

-- Table: PlayerStats
CREATE TABLE PlayerStats (
    PlayerID INT,
    GameID INT,
    Points INT,
    Assists INT,
    Rebounds INT,
    Steals INT,
    Blocks INT,
    MinutesPlayed INT,
    ThreePointersMade INT,
    ThreePointersAttempted INT,
    CONSTRAINT pk_player_stats PRIMARY KEY (PlayerID, GameID),
    CONSTRAINT fk_player FOREIGN KEY (PlayerID) REFERENCES Players(PlayerID),
    CONSTRAINT fk_game FOREIGN KEY (GameID) REFERENCES Games(GameID)
);
