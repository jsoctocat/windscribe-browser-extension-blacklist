# Windscribe Browser Extension with Blacklist function

The official Windscribe Browser Extension only comes with a whitelist/allowlist function that allows any website to bypass the proxy connection once whitelisted. However, quite a few people have been asking for a blacklist function on Discord, Reddit, and someone even opened up an [issue](https://github.com/Windscribe/browser-extension/issues/10) within the official repository.

This fork contains only the files that change 'whitelist' to 'blacklist'.

### (Firefox) If you would like to directly edit the extension without build and sign one then you must use the developer edition of Firefox
1. Click the 3 lines top right
2. Help
3. More troubleshooting information
4. Open Profile Folder
5. Open "extensions" folder
6. Open "@windscribeff.xpi" with 7-Zip (archive)\
7. static -> js -> vendors.chunk.js
8. Search for the following string
9. if ("disconnected" === 
10. Change function name(e.url) to e.originUrl
11. Search for the following string
12. return ".windscribe.com" !== 
13. Delete everything inside the array for variable name = ["????????????"].concat(variable name);
14. Add a 
15. !
16. in front of ?.some(function (t) {

If you are not sure which function/variable to edit, try reference to the JS files from this fork and the official depository and look at the difference.
