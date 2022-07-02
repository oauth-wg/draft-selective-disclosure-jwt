# Selective Disclosure for JWTs (SD-JWT)

This document specifies conventions for creating JSON Web Token (JWT)
documents that support selective disclosure of claim values. 

Written in markdown for the [mmark processor](https://github.com/mmarkdown/mmark).

This is a GitHub repository for a draft specification in [IETF OAuth WG](https://datatracker.ietf.org/doc/draft-fett-oauth-selective-disclosure-jwt/)
For the latest version of the IETF draft, please see https://datatracker.ietf.org/doc/html/draft-fett-selective-disclosure-jwt

For the current version in this repository, see [main.md](main.md) or [github.io](https://oauthstuff.github.io/draft-selective-disclosure-jwt/draft-fett-selective-disclosure-jwt-00.html) for an HTML version.

## Updating Examples

All examples in the document are created from [actual running code](demo/simple.py). To run this code, install jwcrypto library, e.g., like so:
```
pip3 install jwcrypto
```

On Debian/Ubuntu systems, you can instead use the packaged version:
```
sudo apt install python3-jwcrypto
```

You can then run the code (from the root of this repository):
```
python3 -m demo.simple
```

To update the examples in [main.md](main.md), use the provided script:
```
./update-all-examples.sh
```

It calls the demos with the switch `--replace` to replace the example code in
[main.md](main.md) and `--no-randomness` to ensure that the examples are always
generated in the same way (this minimizes the changes that need to be tracked).

The code creates a backup before modifying [main.md](main.md) in [main.md.bak](main.md.bak).

## Compiling

### Using Docker (recommended)
From the root of this repository, run
```bash
docker run -v `pwd`:/data danielfett/markdown2rfc main.md
```
(see https://github.com/oauthstuff/markdown2rfc)

### without Docker
compile using mmark and xml2rfc: `mmark main.md > draft.xml; xml2rfc --html draft.xml`

# Implementations

 * Python: [Reference/Demo Implementation](https://github.com/oauthstuff/draft-selective-disclosure-jwt)
 * Kotlin: [SD-JWT-Kotlin](https://github.com/IDunion/SD-JWT-Kotlin)
 * Rust: [sd_jwt](https://github.com/kushaldas/sd_jwt)

