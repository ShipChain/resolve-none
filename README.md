# resolve-none

This empty package is intended to be used as a replacement for troublesome optional dependencies when resolving packages with Yarn.

#### Example:

Installing loom-js within an alpine-based docker image will fail due to an optional dependency on `@ledgerhq/hw-transport-node-hid` from `@binance-chain/javascript-sdk`.  This can be addressed by installing several alpine packages to enable the builds to succeed; however if the end-user loom-js does not intend to use the ledger support with the binance integration in loom, then these are extra build steps that are not required.  The other approach (that was the impetus for this repo) is to use yarn's `resolutions` property to override the optional dependency with an empty package.  This empty pacakge can be used for "resolving nothing".
