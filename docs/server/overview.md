# Server Configuration

The Gambit-Framework is split into 2 parts. The client and teamserver. The teamserver is the core component that starts and manages listeners, handles implants and their sessions, and handles connections from operators. The main point of configuration for the teamserver is through the server profile.

## Server Profile

Gambit's server profile is the initial configuration for a teamserver. This includes where the server should bind to, operators, and initial configurations for listeners. Note that any changes made such as adding new users, changing passwords, or starting new listeners will not be reflected in the profile. However, the server will search for an existing database before using the profile, so if the server goes down for any reason, it'll spin back up cleanly. You can also export an updated profile based on any changes made.

### Profile Language

Gambit's server profile uses [KDL](https://kdl.dev/) as its configuration language.

### Checking for Errors

Gambit comes with a program `g2lint` (shamelessly stole the name from cs) to check for errors in your server profile.
