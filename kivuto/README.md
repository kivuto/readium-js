readium-js: Kivuto Fork
-----------------------

### Differences

* Uses [Kivuto's readium-shared-js fork](https://github.com/kivuto/readium-shared-js)

### Building

The `kivuto` subfolder contains a shell script that combines the following steps. It was written as a bash script as it uses the gnu patch program. If on Windows, use Git Bash (part of Git for Windows).

1. Copy plugins-override.cson file into place under readium-shared-js (includes highlights plugin, omits hypothesis).
2. Invokes `npm run prepare:all`.
3. Patches jQuery under readium-shared-js with fixes to Sizzle (IE11 getComputedStyle crash, IE permission denied on navigation).
4. Invokes `npm run build` with plugin overriding in place.