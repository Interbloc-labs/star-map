# 🌌

## the star map

a repository of statically-linked Cosmos chain binaries, tracking (a fork of) the [cosmos chain registry](https://github.com/cosmos/chain-registry)

no dependencies needed, just download and go.

note: currently only supports linux/amd64

## direct download

[autobuild.interbloc.org](https://autobuild.interbloc.org)

## apt repo

add repo gpg key (requires curl and gpg)
```
curl -sL https://github.com/InterblocDAO/star-map/raw/%E2%9C%A8/release/repo.key |
  gpg --dearmor | tee /etc/apt/trusted.gpg.d/star-forge.gpg > /dev/null
```
add apt source list
```
echo "deb [arch=amd64 signed-by=/etc/apt/trusted.gpg.d/star-forge.gpg] https://deb.interbloc.org stable main" |
  tee /etc/apt/sources.list.d/star-forge.list > /dev/null
```

install executables with apt
```
apt update
apt install gaiad osmosisd
```

the "suite" (`stable` in the above example) can be modified. please note that supported executables may not be available for all suites

suite | ledger | goleveldb | pebbledb | skip mev
 :--- | :---: | :---: | :---: | :---:
**stable** | ✅ | ✅ | ❌ | ❌
**mev** | ✅ | ✅ | ❌ | ✅
**experimental** | ❌ | ❌ | ✅ | ❌
**experimental_mev** | ❌ | ❌ | ✅ | ✅
