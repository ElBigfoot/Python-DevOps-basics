## Chapter 12
Docker  

Containers share a kernel 
There are two ways to automate Docker using Python 

1) As subprocess library and the use docker CLI (Low Option)
   * You need absolute control over specific CLI commands not readily available in dockerpy.
   * You have a simple script that only utilizes a few basic Docker commands and doesn't require complex object interaction with the Docker Engine. 
  
2) dockerpy 
For most cases, dockerpy is recommended: It simplifies Docker interaction, improves code readability, and provides built-in error handling and type safety.
Here's a breakdown of the pros and cons between dockerpy and the combination of Python subprocess and docker CLI:

**dockerpy (Python library for Docker API):**

**Pros:**

* **Higher-level abstraction:** Provides a more Pythonic interface for interacting with the Docker Engine. Easier to manage containers, images, networks, etc. with code that reads cleaner.
* **Type safety and autocompletion:** Enforces data types for function arguments, improving code reliability and providing autocompletion in IDEs.
* **Exception handling:** Handles errors and exceptions from the Docker Engine more gracefully compared to parsing the raw output of the CLI.
* **Feature completeness:** Offers a comprehensive set of functionalities to manage all aspects of Docker.

**Cons:**

* **Dependency:** Requires installing the `dockerpy` library, adding another dependency to your project.
* **Potential for abstraction overhead:** Depending on your needs, the abstraction layer might introduce some overhead compared to the direct CLI approach.

**Python subprocess + docker CLI:**

**Pros:**

* **Lightweight:** No additional library installation required.
* **Flexibility:** Offers full access to all docker CLI commands, enabling you to leverage any functionality available in the CLI.
* **Direct control:** Provides the most granular control over Docker commands, useful for specific scripting needs.

**Cons:**

* **Lower-level:** Requires parsing the raw output of the CLI commands, making code less readable and potentially error-prone.
* **No type safety:** No automatic type checking for arguments, increasing the risk of errors if arguments are not formatted correctly.
* **Limited exception handling:** Requires manual parsing of error messages from the CLI, making error handling more cumbersome.
* **Feature discovery:** Finding the appropriate Docker CLI command for specific tasks can be challenging, especially for less familiar users.

**Choosing between dockerpy and subprocess + docker CLI:**

* **For most cases, dockerpy is recommended:** It simplifies Docker interaction, improves code readability, and provides built-in error handling and type safety.
* **Use subprocess + docker CLI if:**
    * You need absolute control over specific CLI commands not readily available in dockerpy.
    * You have a simple script that only utilizes a few basic Docker commands and doesn't require complex object interaction with the Docker Engine.

Ultimately, the best choice depends on your specific project requirements and the level of abstraction you need. If you're working with Docker extensively within your Python code, dockerpy is a powerful and reliable option. However, for very basic scripting tasks, the subprocess approach with the docker CLI might suffice.


### create table
