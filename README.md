# SQL-Drills

CREATE SCHEMA starwars;
USE starwars;

CREATE TABLE empire (
	id INT AUTO_INCREMENT,
    name VARCHAR(60) NOT NULL,
    species VARCHAR(60) NOT NULL,
    affilation VARCHAR(100) NOT NULL,
    hierarchy VARCHAR(60) NOT NULL,
    created_at DATETIME DEFAULT CURRENT_TIMESTAMP,
    PRIMARY KEY (id)
);


INSERT INTO empire ( name, species, affilation, hierarchy) VALUES
('Darth Vader', 'Human', 'Galactic Empire', 'Sith Lord'),
('Grand Moff Tarkin', 'Human', 'Galactic Empire', 'Grand Moff'),
('Emperor Palpatine', 'Human', 'Galactic Empire', 'Emperor'),
('General Veers', 'Human', 'Galactic Empire', 'General'),
('Admiral Piett', 'Human', 'Galactic Empire', 'Admiral'),
('Captain Needa', 'Human', 'Galactic Empire', 'Captain');

SELECT * FROM empire;

UPDATE empire SET hierarchy = 'Grand Master 50-Cent' WHERE id = 3;

SELECT * FROM empire;

DELETE FROM empire WHERE id = 4;

SELECT * FROM empire;

