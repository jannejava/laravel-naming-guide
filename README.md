# Laravel naming guide WIP
After researching Laravel's documentation and various repositories, I've compiled a list of best practices and conventions that seem to be more or less a consensus within the Laravel community. Some of these practices, like the Eloquent conventions, are widely accepted, while others are more subject to personal preference. I created this list as a reference for myself and fellow Laravel developers.

If you have any suggestions, please feel free to contribute or share your thoughts.


| Type            | Rule                      | Suffix                        | Example  |
| --------------- |---------------------------|-------------------------------| ---------|
| Class           | PascalCase                |                               | *MyClass.php*              |
| Controller      | singular                  | Controller                    | *PostController.php*       |
| Model           | singular,                 |                               | *Post.php*                  |
| Table           | plural, snake_case        |                               | *user_posts*                    |  
| Columns         | singular, snake_case      |                               | *created_at, user_id*            |
| Route           | plural                    |                               | *users/{username}/ban*          | 
| Named route     | dot-notation, snake-case  |                               | *settings.team* |
| Method          | camelCase                 |                               | *getUsersPosts()*           |
| Variable        | camelCase                 |                               | *$post*                     |
| View            | kebab-case                |                               | *session-expired.blade.php* |
| Config          | kebab-case                |                               | *services-stripe.php*       |
| Event           | *subject for event*       | *a verb*                      | *TeamDeleted.php*      | 
| Provider        |                           | Provider                      | *AppServiceProvider.php* |
| Command         |                           | Command                       | *InstallCommand.php* |
| Request         |                           | Request                       | *CreateTokenRequest.php* |
| Listener        | *descriptive*             | Notification?                 | *UpdateTrialEndingDate.php, SendShipmentNotification.php* |
| Repository      |                           | Repository                    | *UserRepository.php* |
| Asset           | kebab-case                |                               | *vue-bootstrap.js* |
| Helper          | snake_case                |                               | *array_has()* |

All classes uses PascalCase


## Explanations
This is an attempt to explain the origins of the naming standard. Feel free to add to this.

- Helper functions are named in snake_case because of PHP functions are named like this.
- Tables are pluralised because they represent multiple instances of data - each instance being an individual row inside the table.
- Models are named singularly because they represent a single instance, not a collection.
- Suffixs are used to differ, for an example, a repository from a model by just glancing over the file name in your editor.
