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
