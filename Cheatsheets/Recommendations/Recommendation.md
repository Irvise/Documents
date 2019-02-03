# Introducction

This is a simple list containing quick guides to make a decission regarding different aspects of the technological world. If you want just a list of libre alternatives, please, refer to my [libre list](https://github.com/Irvise/Documents/blob/master/Cheatsheets/Libre/Packages.md).

## Disclaimer

This list is created based on my own experience (or even lack thereof). Take everything with a pich of salt and more of a recommendation, rather than anything that I am telling you to do. Always, always do what works for you.

## Choosing a programming language

This list should be used by reading from top to bottom and selecting the first language which suits the requirements.

* **Lua** use it as an scripting language and to extend software where the user is not expected to write performing code. It is easily embeddable in any language.

* **Julia** as a quick way to interact whit programs and write performant systems (unless the languages below suit that requirement better). If python is good for that job (unless Lua suits it better), then you should use **Julia**. It should also be embedded as an user programming interface in more complex software where the user is expected to write quite some code.

* **Golang** for web related services where performance is important. By performance I mean that the backend will have to do some heavy lifting tasks and the user should not be left waiting.

* **Elixir/Erlang** for web services where stability and scalability need to be ensured. Efficiency nor performance should be the main characteristic for the project. Consider using the [Phoenix Framework](https://phoenixframework.org/) and [Drab](https://tg.pl/drab).

* **Elm** for front end. However, consider if it is trully necessary to write one using something other than a static website generator and or through the backend.

* **FORTRAN** if the program has to be as performant as possible, and it will mainly consist on (math/logic) operations, rather than data management. Use modern fortran, it is more flexible, clearer and has wonderful types. Please, take a look into CoArrays, OpenMP and OpenMPI.

* **C** for embedded devices or resource constrained systems; when performance is of paramount importance. Please, use C99 or newer. And take your time to learn it.

* **Rust** when the program is of great complexity, requires to be correct (code-bug-free), and performant.

* **Ada/Spark** for critical software where not just the code but the logic has to be correct.

* **Prolog** when the problem faced is easier with a logical approach. Also, anything AI.

* **LISP/SCHEME** when the complexity of the problem outgrows the necessity of performance. As an extra addition, it is a joy to write.

* **Assembly** when there is nothing that will suit the performace. Or just to have access to all the functionallity that the hardware has to offer. It is also great fun writting it when done as a hobby, and you will learn more than what you would have imagined.

### Databases

* **SQLite** for simple projects.

* **PostgreSQL** for any project where the schema is well defined and performance is a must.

* **Redis** in memory database.

* **TODO** expand descriptions and are other types.

## Formats

