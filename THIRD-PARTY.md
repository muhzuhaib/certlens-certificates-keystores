# Third-party dependencies and their licences

Every runtime dependency shipped inside the plugin zip, with the licence read from the jars that are
actually shipped rather than from memory. Checked 2026-09-24 against the 2026.1.0 build.

The zip ships five jars: the plugin's own two (`certlens-ide-2026.1.0.jar`, `certlens-core.jar`)
and the three below.

| Dependency | Version | Licence | Why it is here |
| --- | --- | --- | --- |
| `org.bouncycastle:bcprov-jdk18on` | 1.86 | MIT | Reading and building keys and certificates, and the formats the JDK alone does not read |
| `org.bouncycastle:bcpkix-jdk18on` | 1.86 | MIT | PKCS#10 signing requests, PKCS#7 bundles and certificate generation |
| `org.bouncycastle:bcutil-jdk18on` | 1.86 | MIT | Shared ASN.1 utilities that bcpkix depends on |

All three are redistributed unmodified. The Kotlin standard library is not bundled; the IntelliJ
Platform provides it.

## The Bouncy Castle licence

The MIT licence requires its copyright notice and permission notice to be included with every copy.
**It is included in the plugin you install**: each of the three jars carries it as
`META-INF/LICENSE.md` (the three files are identical). It is reproduced here in full:

> MIT License (https://opensource.org/licenses/MIT)
>
> Copyright (c) 2000-2026 The Legion of the Bouncy Castle Inc. (https://www.bouncycastle.org).
>
> Permission is hereby granted, free of charge, to any person obtaining a copy of this software and
> associated documentation files (the "Software"), to deal in the Software without restriction,
> including without limitation the rights to use, copy, modify, merge, publish, distribute, sub
> license, and/or sell copies of the Software, and to permit persons to whom the Software is
> furnished to do so, subject to the following conditions: The above copyright notice and this
> permission notice shall be included in all copies or substantial portions of the Software.
>
> THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT
> NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND
> NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM,
> DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT
> OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

**MIT is compatible with a paid closed-source plugin.** It asks only that the notice travel with the
copies, which it does. It does not require our own source to be published.

## Not shipped, and not depended on either

CertLens depends on `com.intellij.modules.platform` and nothing else: no language plugin and no
Database or Ultimate-only module, which is what lets it install in every JetBrains IDE.
