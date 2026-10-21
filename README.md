CHERRY BLOSSOM CLIENT 2.1
Every Minecraft version, Alpha to 26.3
========================================

STARTING
  Double-click "Cherry Blossom Client.exe".
  The first time, it downloads a small Java to run the launcher (about 56 MB).
  Each Minecraft version downloads once, the first time you play it, along
  with the exact Java that version needs (Java 8, 17, 21 or 25).

  Windows may say "Windows protected your PC" because the exe isn't
  code-signed. Click "More info" then "Run anyway".

  Everything stays inside this folder. Your normal .minecraft is never
  touched. To uninstall, delete the folder.


LANGUAGE / JĘZYK
  The launcher speaks English and Polish. It starts in Polish if Windows
  is set to Polish. Switch any time: Settings > Launcher > English / Polski.
  Launcher działa po polsku i po angielsku. Zmiana: Ustawienia > Launcher.

THE LAUNCHER
  Home ......... the big Launch button, Quick join servers, recently played
                 versions and a summary of your setup
  Versions ..... every release from 1.0 to 26.3, plus Beta, Alpha and all
                 snapshots. Pick a version, the exact patch, and Fabric or
                 Vanilla. Search works by number or name ("1.8.9", "Trails")
  Mods ......... the Cherry HUD and a curated set of mods from Modrinth,
                 showing which ones exist for the version you picked
  Settings ..... PC preset, memory, player name, game window size

  Each version family (1.21, 1.20, 1.8 ...) has its own folder for worlds,
  options and resource packs, so an old version can never damage a newer
  world. Each exact version has its own mods folder.


HOST YOUR OWN SERVER (Server page in the sidebar)
  Pick a version (1.2.5 to 26.3), drag the memory slider (it suggests an
  amount for your PC), set name, players, port, difficulty and game mode,
  tick the Minecraft EULA, and press Start server. It downloads the
  official server from Mojang and the right Java, then runs with tuned
  memory settings and a view distance your CPU can handle.
  - The console shows the server log; type commands like "op YourName".
  - Join opens the game straight into your server (localhost).
  - "Microsoft accounts only" off = offline players can join.
  - Friends on your Wi-Fi join with your PC's local IP. For friends
    elsewhere, forward the port (25565) on your router.
  - Worlds live in data\servers\<version>. Closing the launcher saves
    and stops the server.

PRESETS (Settings > Performance)
  The launcher looks at your RAM and CPU and suggests one.

  Low-end ..... 2 GB, G1 garbage collector, Sodium, Lithium, FerriteCore,
                ModernFix, ImmediatelyFast, Entity Culling, More Culling,
                Dynamic FPS and more. Video: render distance 6, fast
                graphics, minimal particles, no clouds.
  Balanced .... 4 GB, the same core mods. Render distance 10.
  High-end .... 6 GB, ZGC (smoothest frame times), plus C2ME (chunk loading
                on all cores), Iris shaders and dynamic lights. Distance 16.
  Custom ...... change any mod or the memory slider yourself.

  Video settings are written once, on the next launch, and only if
  "Apply the preset's video settings" is on. After that they're yours.

  Mods only work with Fabric, which starts at 1.14. Older versions run
  vanilla. If a mod hasn't been made for a version, it's skipped, and
  anything a mod needs is downloaded with it.


FRIENDS (sidebar > Friends, or U in game)
  Works for offline players too: nobody needs a Microsoft account.
  - Your friend code (like ABCD-EFGH-JKLM-NPQR) is on the Friends page.
    Send it to a friend, they paste it in "Add a friend". Or type their
    player name; that works if they opened Cherry in the last 12 hours.
  - They get a request (pop-up in game too) and press Accept.
  - The list shows who's online and what they're doing ("On
    mc.hypixel.net (1.21.11)"). Join puts you on the same server with the
    same version.
  - In game: U (or Right Shift > Friends) to add, accept and remove.
    The in-game part is in 1.21.9 to 26.3, like the HUD; the launcher
    page works for every version.
  - Requests and status travel through ntfy.sh, a free public relay.
    Every message is signed with your own key (data\friends.json), so
    no one can pretend to be you. Don't share that file. Friends can see
    which server you're on while you play.


AUTOMATIC UPDATES
  The launcher checks for a new version when it starts and every few
  hours. When one is ready, "Update x.y ready: restart" shows at the
  top; click it and the client restarts on the new version.

  To publish updates to everyone who has your client:
    1. Make a free GitHub account and a public repository, for example
       "cherry-blossom-client".
    2. Open launcher\update.txt and put  YourName/cherry-blossom-client
       on its own line. Do this BEFORE you give the client to people.
    3. For each update: on GitHub, Releases > Draft a new release, tag it
       with a higher version than before (this build is v2.1.0, so the
       next is v2.2.0), attach the new launcher\cherry-launcher.jar,
       and Publish. Everyone gets it the next time they open the client.
  Only the launcher updates itself this way (it carries the HUD mod and
  shaders inside it). The .exe stays the same.


SHADERS (E-LITE shaders 5.1.1, built in)
  The E-LITE pack ships inside the client. On any Fabric version that Iris
  supports (about 1.16 and up), Iris + Sodium are installed and the pack
  is switched on for you the first time you play. Nothing to download.
  - K in game ......... shaders on / off
  - O in game ......... shader settings (quality, shadows, etc.)
  - Low-end PC? Press K to turn them off, or untick "E-LITE shaders" on
    the Mods page. Picking another pack in game is remembered.
  E-LITE is LGPL-3 licensed by its authors.


IN GAME (Cherry HUD: 1.21.9 to 26.3)
  Title screen ........ Cherry's own: Singleplayer, Multiplayer, Options,
                        Quit, and an icon bar for the Cherry menu, HUD
                        layout, Realms, Language and Accessibility.
                        Turn it off in Right Shift > Look if you prefer
                        the vanilla one.
  Right Shift ......... open the Cherry menu
     HUD tab .......... 16 widgets: FPS, Ping, Server, CPS, Keystrokes,
                        Armor Status, Potion Effects, Coordinates,
                        Direction, Biome, Speed, Saturation, Clock,
                        Session Time, Memory, Sprint Status
     Features tab ..... toggle sprint, zoom options, 24-hour clock
     Look tab ......... background, text shadow, colour values, accent
  Edit HUD Layout ..... drag widgets anywhere; they snap to the centre and
                        to each other. Scroll to resize, right-click to
                        hide, R to reset, Esc to save.
  Hold C .............. zoom. Scroll while holding to zoom further.

  Rebind keys in Options > Controls > Cherry Blossom Client.


ACCOUNTS
  Offline: set a player name in Settings. Works for singleplayer, LAN and
  servers that allow offline players.

  Microsoft (for servers like Hypixel): Microsoft only lets approved apps
  sign in to Minecraft, so you need your own free Azure app ID:
    1. portal.azure.com > App registrations > New registration,
       "Personal Microsoft accounts only"
    2. Authentication > "Allow public client flows" = Yes
    3. Ask for Minecraft API access: https://aka.ms/mce-reviewappid
    4. When approved, Settings > "Sign in with Microsoft", paste the ID.
  You sign in on Microsoft's own page. Tokens are saved in
  data\cherry-launcher.json, so don't share that file.


DISCORD (shows "Playing Cherry Blossom Client" on your profile)
  Works out of the box with the Cherry Blossom Client Discord app.
  Opening the launcher shows you in the client; in game it shows the
  version, the server (with Quick join) and how long you've played.
  Keep the Discord desktop app running.

  For the blossom picture on your profile, the app owner uploads
  discord-logo.png once: discord.com/developers/applications >
  Cherry Blossom Client > Rich Presence > Art Assets > Add Image,
  named exactly:  logo

  Turn it off in Settings > Launcher > "Show on Discord".

KNOWN LIMITS
  - Offline accounts on 1.16.4 and 1.16.5 may see Multiplayer greyed out.
    That's the game itself checking for a Microsoft account.
  - The Cherry HUD exists for 1.21.9 to 26.3. Other versions still get the
    performance mods (from 1.14 up) but not the HUD.


FOLDERS
  launcher\            the launcher
  runtime\             Java for the launcher
  data\instances\      worlds, options, packs and mods, one folder per version family
  data\runtime\        Java for each Minecraft version
  data\versions\, data\libraries\, data\assets\   game files, shared by all versions
  source.zip           full source: HUD mod, launcher and exe
