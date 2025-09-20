# Server Core 🧠

* **Module:** `server`
* **Depends on:** `networking`, `protocol`, `plugin-api` (if you are building it alongside)
* **Resources:** Knowledge of game development concepts like game loops, entity-component systems, and event handling is
  key.
* **What you should look at:**
    * **The Game Loop:** This is a crucial concept. The server operates on a fixed tick rate (typically 20 ticks per
      second). The game loop processes all pending actions for that tick. This includes player movements, entity AI, and
      block updates.
    * **World Management:** Create data structures to represent your world. Chunks are a fundamental unit in Minecraft.
      You'll need to load, save, and manage the state of these chunks. This is where you'll store block data, biomes,
      and other world-specific information.
    * **Entity System:** Manage players, mobs, and other non-block entities. This system tracks their position, health,
      inventory, and behavior. You'll need a way to efficiently query and update entities.

-----

# Application 🖥️

* **Module:** `server`
* **Depends on:** `networking`, `plugin-api`
* **Resources:** Your build tool, like **Gradle**, will be key here.
* **What you should look at:**
    * **Main Class:** This module will contain the `main` function that starts your server.
    * **Configuration:** Handle server settings from a file (e.g., `server.properties`). This includes things like the
      MOTD, server port, and max players.
    * **Dependency Injection:** Use a lightweight DI framework like **Koin** to wire your modules together. This makes
      the codebase more testable and easier to manage.