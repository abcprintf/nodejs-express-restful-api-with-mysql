## Create Database and table
```sh
-- Table structure for users
  CREATE TABLE IF NOT EXISTS users (
    id int(11) NOT NULL,
    name varchar(200) NOT NULL,
    email varchar(200) NOT NULL,
    created_at datetime NOT NULL DEFAULT CURRENT_TIMESTAMP
  ) ENGINE=InnoDB DEFAULT CHARSET=latin1;
  ALTER TABLE users ADD PRIMARY KEY (id);
  ALTER TABLE users MODIFY id int(11) NOT NULL AUTO_INCREMENT;
```

## Insert data to database
```sh
INSERT INTO users (id, name, email, created_at) VALUES
  (1, 'test', 'test@gmail.com', '2019-02-28 13:20:20'),
  (2, 'john', 'john@g.com', '2019-02-28 13:20:20'),
  (3, 'mix', 'mix@mail.com', '2019-02-28 13:20:20'),
  (4, 'ioio', 'ioio@g.co.th', '2019-02-28 13:20:20'),
  (5, 'popo', 'popo@g.co.th', '2019-02-28 13:20:20');
```

## methods name
|  Method |  Method |  Method |
|---|---|---|
|   GET   | /users  |   	fetch all users |
|   GET   | user/1  |   fetch user with id ==1  |
|   POST  | user    |   add new user    |
|   PUT  |  user    |   update user by id == 1  |
|   DELETE  |   user    |   delete user by id == 1  |