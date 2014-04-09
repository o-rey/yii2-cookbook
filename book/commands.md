Commands and background tasks
=============================

Sometimes we need to perform tasks that are not related to user interacion directly. For example:

- Mass-mailing
- Backup
- Data export and import
- Images processing
- DB cleanup

and so on.

We can use commands for that.

Configuring console
-------------------

TBD

Creating a command
------------------

Yii is shipped with an example of console command, `/commands/HelloController.php`. You can use this file as a boilerplate for writing your own commands.

Let's create a simple command, that exports our table to csv.

Start with creating a file `commands/ExportController.php`:

```php
namespace app\commands;

use yii\console\Controller;

class ExportController extends Controller
{
    public function actionIndex()
    {
        echo "done!\n";
    }
}
```

Now switch to your application folder and run `./yii` (`yii.bat` if you're on Windows)
You'll see `export` command along with some core commands (asset, cache, message and so on).

Now if you run `./yii export` you should see our "done!" message. This means that everything works as expected.

Now let's add some useful stuff.
Good thing about commands is that they're very similar to web controllers, so you can use most of the well-known functions.

Running a command
-----------------

TBD

Creating cronjob
----------------

TBD

See also
--------

TBD
