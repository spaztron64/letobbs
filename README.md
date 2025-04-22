# LetoBBS

LetoBBS is the second message board software written in PHP mainly for the AkiChannel boards. It's purpose is to replace the currently active JesenBBS board software, maintaining it's core features while not repeating some of it's more critical development mistakes.

Core strengths identified in JesenBBS that will remain in LetoBBS:
- No reliance on client-side code
- Page layout and size efficiency
- A proper user system. No reliance on tripcodes and hacked-together admin users
- A user permission level system
- A locale system that allows localization of GUI elements
- Designed to be usable in shared site environments. Can be deployed on dedicated subdomains or subdirectories within one domain

Issues identified in JesenBBS that require resolution in LetoBBS at a foundational level:
- MySQL as a hard dependency. Switch to PDO
- Designed around Apache web server environments. Must consider other web servers
- Overreliance on <div>s. The Futaba-like layout is best suited to <table>s instead, which also increases compatibility with text-based browsers like Links
- Insufficient modularity. Too much code is repeated across TUs
- Poorly written functions. Many functions consist of dozens of haphazardly written echo statements.
- Overly minimal styling

Potential issues that may or may not be resolved:
- No static content generation and display pipeline, all requests invoke PHP. Could present scalability issues

Full production for this project has yet to begin.
