# rest-api-with-lumen Vagrant

This project can be used as Vagrant configuration for a webapp created with [rest-api-with-lumen boilerplate](https://github.com/hasib32/rest-api-with-lumen).

The configuration has been created using [puphpet](https://github.com/puphpet/puphpet).

## Getting Started

Place your `rest-api-with-lumen` project dir in `awesome` directory.
Your directory tree should look like this:
```
root
│   ...
│
└───html
└───puphet
└───awesome
│   │
│   └───rest-api-with-lumen_project
│       │   └───public
│       │   ...
│   
```

In order to enable Virtual Host for your web app, add this line in your hosts file (your machine, not the VM):
```
192.168.56.101 awesome.dev www.awesome.dev
```

## Final step

To allow your project to be served from apache, enter in VM and edit `25-rest_api_with_lumen.conf`.
Replace every occurrence of `/var/www/awesome` with `/var/www/awesome/rest-api-with-lumen_project/public` where `rest-api-with-lumen_project` is your rest project name.

Finally restart apache with
```
sudo service apache2 restart
```

## License
This project is licensed under the [MIT license](LICENSE).