# gradle-add-credentials

Dummy project to call the `addCredentials` task of the [gradle-credentials-plugin](https://github.com/etiennestuder/gradle-credentials-plugin) globally.

Just call:

    $ gradle addCredentials --key someKey --value someValue

Then in any other project the credentials are available using `credentials.someKey`.

Use it if a project uses for example authenticated dependencies. You can't call the plugin task because the configuration phase already wants to resolve project dependencies, for which you need the credentials...