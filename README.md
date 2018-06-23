# Laravel naming guide WIP
After digging in Laravel's documentation and some other repositories, this seems to be more or less a consensus. Some go without saying like the Eloquent conventions, others are more up to you. I made this list for my self. 

If you have any suggestions, let me know.

| Type            | Rule                      | Suffix                        | Example  |
| --------------- |---------------------------|-------------------------------| ---------|
| Class           | PascalCase                |                               | *MyClass.php*              |
| Controller      | singular                  | Controller                    | *PostController.php*       |
| Model           | singular,                 |                               | *Post.php*                  |
| Table           | plural, snake_case        |                               | *user_posts*                    |  
| Columns         | plural, snake_case        |                               | *created_at*                     |
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
| Repository      |                           | Repository                    | *UserRepositry.php* |
| Asset           | kebab-case                |                               | *vue-bootstrap.js* |
| Helper          | snake_case                |                               | *array_has()* |

All classes uses PascalCase
