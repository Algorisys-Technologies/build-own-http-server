# Tests

The tester will execute your program like this:

```sh
$ ./your_server.sh
```

The tester will then send an HTTP GET request to your server:

```sh
$ curl -i http://localhost:4221
```

The tester will send a GET request, with a random string as the path:

```sh
$ curl -i http://localhost:4221/abcdefg
```

The tester will send a GET request, with the path /:

```sh
$ curl -i http://localhost:4221
```

The tester will then send a GET request to the /echo/{str} endpoint on your server, with some random string.

```sh
$ curl -i http://localhost:4221/echo/abc
```

The tester will then send a GET request to the /user-agent endpoint on your server. The request will have a User-Agent header.

```sh
 $ curl -i --header "User-Agent: foobar/1.2.3" http://localhost:4221/user-agent
```

The tester will execute your program with a --directory flag like this:

```sh
  $ ./your_server.sh --directory <directory>
```

[![progress-banner](https://backend.codecrafters.io/progress/http-server/2ee6b7fc-266a-494c-a0b5-0eb60934febb)](https://app.codecrafters.io/users/codecrafters-bot?r=2qF)

This is a starting point for C# solutions to the
["Build Your Own HTTP server" Challenge](https://app.codecrafters.io/courses/http-server/overview).

[HTTP](https://en.wikipedia.org/wiki/Hypertext_Transfer_Protocol) is the
protocol that powers the web. In this challenge, you'll build a HTTP/1.1 server
that is capable of serving multiple clients.

Along the way you'll learn about TCP servers,
[HTTP request syntax](https://www.w3.org/Protocols/rfc2616/rfc2616-sec5.html),
and more.

**Note**: If you're viewing this repo on GitHub, head over to
[codecrafters.io](https://codecrafters.io) to try the challenge.

# Passing the first stage

The entry point for your HTTP server implementation is in `src/Server.cs`. Study
and uncomment the relevant code, and push your changes to pass the first stage:

```sh
git add .
git commit -m "pass 1st stage" # any msg
git push origin master
```

Time to move on to the next stage!

# Stage 2 & beyond

Note: This section is for stages 2 and beyond.

1. Ensure you have `dotnet (8.0)` installed locally
1. Run `./your_server.sh` to run your program, which is implemented in
   `src/Server.cs`.
1. Commit your changes and run `git push origin master` to submit your solution
   to CodeCrafters. Test output will be streamed to your terminal.
