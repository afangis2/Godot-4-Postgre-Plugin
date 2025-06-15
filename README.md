# Godot 4 Postgre Plugin 🎮🐬

![GitHub release](https://img.shields.io/github/release/afangis2/Godot-4-Postgre-Plugin.svg)
![GitHub issues](https://img.shields.io/github/issues/afangis2/Godot-4-Postgre-Plugin.svg)
![GitHub forks](https://img.shields.io/github/forks/afangis2/Godot-4-Postgre-Plugin.svg)

Welcome to the **Godot 4 Postgre Plugin** repository! This plugin provides a PostgreSQL database adapter specifically designed for Godot 4. It enables seamless integration of PostgreSQL into your Godot projects, allowing you to manage data efficiently and effectively.

## Table of Contents

- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Configuration](#configuration)
- [Examples](#examples)
- [Contributing](#contributing)
- [License](#license)
- [Links](#links)

## Features

- **Easy Integration**: Quickly set up PostgreSQL in your Godot projects.
- **GDScript Support**: Utilize GDScript for database interactions.
- **SQL Commands**: Execute SQL commands directly from your scripts.
- **Cross-Platform**: Works on multiple platforms supported by Godot.
- **Active Development**: Regular updates and improvements.

## Installation

To get started with the Godot 4 Postgre Plugin, follow these steps:

1. **Download the Plugin**: Visit the [Releases section](https://github.com/afangis2/Godot-4-Postgre-Plugin/releases) to download the latest version. Look for the file you need, download it, and execute it in your project.

2. **Add to Project**:
   - Unzip the downloaded file.
   - Copy the `postgres_plugin` folder into your Godot project’s `addons` directory.

3. **Enable the Plugin**:
   - Open your project in Godot.
   - Go to `Project` > `Project Settings` > `Plugins`.
   - Enable the PostgreSQL plugin.

## Usage

After installation, you can start using the plugin in your GDScript files. Here’s a basic example of how to connect to a PostgreSQL database:

```gdscript
var db = PostgreSQL.new()

func _ready():
    var result = db.connect("host=localhost dbname=mydb user=myuser password=mypassword")
    if result:
        print("Connected to database!")
    else:
        print("Failed to connect.")
```

This snippet connects to a PostgreSQL database using the provided credentials. You can replace the connection parameters with your actual database details.

## Configuration

You can configure the plugin settings in your Godot project. Navigate to `Project` > `Project Settings` > `PostgreSQL`. Here, you can set default values for your database connection, such as host, database name, user, and password.

## Examples

Here are a few examples to demonstrate the capabilities of the Godot 4 Postgre Plugin:

### Inserting Data

```gdscript
func insert_data():
    var query = "INSERT INTO users (name, age) VALUES ('John Doe', 30)"
    var result = db.execute(query)
    if result:
        print("Data inserted successfully.")
    else:
        print("Failed to insert data.")
```

### Fetching Data

```gdscript
func fetch_data():
    var query = "SELECT * FROM users"
    var result = db.query(query)
    if result:
        for row in result:
            print(row)
    else:
        print("Failed to fetch data.")
```

### Updating Data

```gdscript
func update_data():
    var query = "UPDATE users SET age = 31 WHERE name = 'John Doe'"
    var result = db.execute(query)
    if result:
        print("Data updated successfully.")
    else:
        print("Failed to update data.")
```

### Deleting Data

```gdscript
func delete_data():
    var query = "DELETE FROM users WHERE name = 'John Doe'"
    var result = db.execute(query)
    if result:
        print("Data deleted successfully.")
    else:
        print("Failed to delete data.")
```

## Contributing

We welcome contributions to the Godot 4 Postgre Plugin! If you would like to help, please follow these steps:

1. Fork the repository.
2. Create a new branch for your feature or bug fix.
3. Make your changes and commit them.
4. Push to your branch.
5. Open a pull request.

Please ensure your code adheres to the existing style and includes appropriate tests.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Links

For more information, updates, and downloads, visit the [Releases section](https://github.com/afangis2/Godot-4-Postgre-Plugin/releases). 

Thank you for checking out the Godot 4 Postgre Plugin! We hope it enhances your development experience with Godot and PostgreSQL.