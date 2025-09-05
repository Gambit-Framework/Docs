# Server Profile

## `profile` block

The `profile` block holds the metadata for the server profile. This includes the profile's name and a short description.

```kdl
profile {
    name            "example profile"
    description     "example"
}
```

## `server` block

The `server` block holds the configuration for where to host the teamserver. This includes the host and port for the teamserver to bind to. This is where operators will connect to the teamserver using `gambit-client`.

```kdl
server {
    bind-host   "0.0.0.0"
    bind-port   4455
}
```

## `operators` block

The `operators` block holds the usernames and passwords for operators to connect to the teamserver with. It also holds the `root-password` for the default root account.

```kdl
operators {
    root-password   "password"

    user "drngd0tter" {
        password    "password"
    }

    user "0tter" {
        password    "password"
    }
}
```

## `listeners` block

The `listeners` block allows you to start and configure and listeners

```kdl
listeners {
    http "listener-name" {
        bind-host   "0.0.0.0"
        bind-port   80

        user-agent  "Mozilla/5.0 (Windows NT x.y; Win64; x64; rv:10.0) Gecko/20100101 Firefox/10.0"
        headers     "Gambit-Version: 0.1,Authorization: sdjh39abfkl0s"
        uris        "index.php,index.html,about/about.php"
        method      "post"
    }
}
```
