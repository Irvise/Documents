# Introducction

This is a simple list containing quick guides to make a decission regarding different aspects of the technological world. If you want just a list of libre alternatives, please, refer to my [libre list](https://github.com/Irvise/Documents/blob/master/Cheatsheets/Libre/Packages.md).

## Disclaimer

This list is created based on my own experience (or even lack thereof). Take everything with a pich of salt and more of a recommendation, rather than anything that I am telling you to do. Always, always do what works for you.

## Choosing a programming language

This list should be used by reading from top to bottom and selecting the first language which suits the requirements.

* **Lua** use it as an scripting language and to extend software where the user is not expected to write performing code. It is easily embeddable in any language.

* **Julia** as a quick way to interact whit programs and write performant systems (unless the languages below suit that requirement better). If python is good for that job (unless Lua suits it better), then you should use Julia. It should also be embedded as an user programming interface in more complex software where the user is expected to write quite some code.

* **FORTRAN** if the program has to be as performant as possible, and it will mainly consist on (math/logic) operations, rather than memory management, use modern fortran. It is more flexible, clearer and has wonderfully simple yet powerful type system. Please, take a look into CoArrays, OpenMP and OpenMPI.

* **C** for embedded devices or resource constrained systems; when performance is of great importance. Please, use C99 or newer. And take your time to learn it.

* **Ada/Spark** for critical software where not just the code but the logic HAS to be correct.

* **Rust** when the program is of great complexity, has to be correct (code-bug-free), performant and development speed is important.

* **Prolog** when the problem faced is easier with a logical approach. Also, anything AI.

* **LISP/SCHEME** when the complexity of the problem outgrows the necessity of performance. As an extra addition, it is a joy to write.

* **Assembly** when there is nothing that will suit the performace. Or just to have access to all the functionallity that the hardware has to offer. It is also great fun writting it when done as a hobby, and you will learn more than what you would have imagined.

* **Coq/F\*** for formally provable programs. If the program has to be compiled to machine code or other languages, F* is a great choice.

### Systems/Web related

* **Elixir/Erlang** for web services where stability and scalability need to be ensured. Efficiency nor performance should be the main characteristic for the project. Consider using the [Phoenix Framework](https://phoenixframework.org/) and [Drab](https://tg.pl/drab).

* **Golang** for web related services where performance is important. By performance I mean that the backend will have to do some heavy lifting tasks and the user should not be left waiting.

* **Elm** for front end. However, consider if it is trully necessary to write one using something other than a static website generator and or through the backend.

### Databases

* **SQLite** for simple projects.

* **PostgreSQL** for any project where the schema is well defined and performance is a must.

* **Redis** in memory database.

* **TODO** expand descriptions and are other types.

## Formats

### Text files

If it has to be human readable, please, use plain text. Even if the file should, very rarely, be read by a person; still, make it a plain text.

* **Org files** may be used to take advantage of most of the mentioned properties of the above formats. Use it as your hearts desire.

* **TOML** for structured data and configuration.

* **Markdown** for simple documentation texts.

* **TeX** for scientific and formal documentation of projects. Try to keep it as simple and as barebones as possible, don't be fancy. If you need anything more flexible than the default classes, use KOMA. Also, partition your .tex files!

* **ODF** (Open Document Format) for more complex texts and automated forms.

* **PDF or PostScript** for printing or read-only copies.

* **MusicXML** while XML is something that boggles my mind, if you have to exchange music between to programs (such as the wonderful MuseScore or Denemo), use MusicXML, since it is a standard understood by many and works well.

## Editors



## CLI/TUI software