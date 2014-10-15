Utils
=====

Here a collection of utils for increasing your productivity:
* prepare-commit-msg – git hook
* metadata – metadata generator for Xamarin samples

prepare-commit-msg
------------------
Git hook. You will find it a convinient if you store more then one solution within repo (e.x. MyCoolApp.sln and Other.sln). This hook will prefix your commit message with `[MyCoolApp]` if you change some files relative to MyCoolApp project


You need to place this file to `.git/hooks/` dir then provide execution permissions:
`$ chmod 777 .git/hooks/prepare-commit-msg`

metadata
--------
Script will generate Metadata.xml with predefined values for your Xamarin sample. Usage:
`$ ./metadata -ios` – will print generated Metadata for iOS sample
`$ ./metadata -android` – will print generated Metadata for Android sample
`$ ./metadata -wp` – will print generated Metadata for WindowsPhone sample

To simplify usage create a symbolic link:
`ln -s <absolute path to dir>/metadata /usr/local/bin/metadata`
`chmod 777 metadata` – add execution permissions
