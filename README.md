<p align="center">
  <img alt="NetworkExplorer Logo" src="media/nwexp_logo.png" width="125" height="125" />
</p>

<h1 align="center">NetworkExplorer</h1>

NetworkExplorer is a school project created by [@0Adiber][1] and [@TheCrether][2]. It is a NAS for your PC and home server with a nice web interface. It is built with React and Spring Boot.

The application is split up into two different repositories:

- [NetworkExplorer/frontend][3]
- [NetworkExplorer/backend][4]

Each repository has its own instructions on how to build itself and the following is how to put both together.

## Putting it all together

1. First of all, you need to create a directory for the files of the application.
2. Build the [backend][4] ([Instructions][6])
3. Copy your built JAR in the `target` folder into the directory
4. Copy/Create your `application.properties` file and copy it into the directory (Example configuration can be found [here][5]))
5. Build the [frontend][3] ([Instructions][7])
6. Copy the `build` directory from the frontend into the directory and rename it to `public`
7. (Optional) If you tested the project in your IDE and like to keep the credentials/users you setup, you can just copy the `nwexp.json` file from your backend folder.
8. Start the server by executing this command: `java -jar <your-jar> at.networkexplorer.backend.BackendApplication`

If number 7 did not apply to you, the initial admin password will be printed out to the console and if you somehow cleared the output, you can just delete the `nwexp.json` file and start the server again to generate a new password.

[1]: https://github.com/0Adiber
[2]: https://github.com/TheCrether
[3]: https://github.com/NetworkExplorer/frontend
[4]: https://github.com/NetworkExplorer/backend
[5]: https://github.com/NetworkExplorer/backend#configuration
[6]: https://github.com/NetworkExplorer/backend#building-the-jar
[7]: https://github.com/NetworkExplorer/frontend#building-the-project
