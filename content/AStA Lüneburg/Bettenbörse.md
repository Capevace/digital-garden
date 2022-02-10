# Bettenbörse

\#asta #dev z

## `Announcement` Model

ID: `string`
Type: `request` | `offering`
Name: `string`
E-Mail: `string`
Phone: `string`
Gender `string` (optional)

````php
public string $id;
public string $type;
public string $name;
public string $email;
public string $phone;
public ?string $gender;

public array $availableBeds;
public int $availableBedCount;
public ?string $locationHint;
public ?string $wishes;

public \DateTime $from;
public \DateTime $until;
````

## Requests table

````sql

CREATE TABLE couchsurfing_requests (
	`id` CHAR(36) NOT NULL, 
	`type` ENUM('request','offer') NOT NULL, 
	`name` VARCHAR(128) NOT NULL, 
	`email` INT(128) NOT NULL, 
	`phone` VARCHAR(64) NOT NULL, 
	`gender` VARCHAR(128) NULL, 
	`bed_type` VARCHAR(256) NOT NULL, 
	`bed_count` SMALLINT NOT NULL DEFAULT '1',
	`location_hint` VARCHAR(1024) NULL,
	`wishes` VARCHAR(1024) NULL,
	`from` DATE NOT NULL, 
	`until` DATE NOT NULL, 
	
	PRIMARY KEY (`id`), 
	INDEX `TYPE` (`type`), 
	INDEX `FROM` (`from`), 
	INDEX `UNTIL` (`until`)
); 

````

## Database Maintenance:

Delete requests, offers and their matches if the end date is more than 2 months ago.

 > 
 > Matches will be deleted automatically due to cascading foreign keys (`DELETE CASCADE` during table creation).

````sql
DELETE FROM requests WHERE until < (NOW - 2 months)
````
