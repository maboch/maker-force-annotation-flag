## Install

**Enable composer patching**

First step, your composer could be install patch, so you need the following package `cweagans/composer-patches`.

```bash
composer require cweagans/composer-patches
```

**Apply patch**

In your `composer.json`:

```js
{
    // {...} composer.json content
    "extra": {
        "patches": {
            "symfony/maker-bundle": {
                "Provide flag to force annotation in make entity command": "https://raw.githubusercontent.com/maboch/maker-force-annotation-flag/master/maker-force-annotation-flag.patch"
            }
        }
    }
}
```

Now, run `composer update`.

**Use**

Add flag `--force-annotation` in make:entity `command`.
