# HMAC_SHA256

C++ 17 version of HMAC SHA256

Ported from and Credits to:
- [System-Glitch/SHA256](https://github.com/System-Glitch/SHA256)
- [h5p9sl/hmac_sha256](https://github.com/h5p9sl/hmac_sha256)

## Usage

```c++
#include <cassert>
#include <iostream>

#include "hmac_sha256.h"

int main() {
    const std::string data = "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis ornare.";
    const std::string key  = "secret-key";

    const uint8_t *key_bytes  = reinterpret_cast<const uint8_t *>(key.data()),
                  *data_bytes = reinterpret_cast<const uint8_t *>(data.data());

    uint8_t    *bytes_hash = HMAC_SHA256::hmac(key_bytes, key.length(),
                                               data_bytes, data.length());
    std::string hash       = HMAC_SHA256::toString(bytes_hash);
    std::cout << hash << "\n";
    assert(hash == "0aa255a6d8364f5cb9dc2b5893b31f03ea186d2b687d045b2b16c3098b7ff6b5");

    return 0;
}
```
