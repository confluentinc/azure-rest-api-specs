## Ruby

These settings apply only when `--ruby` is specified on the command line.

``` yaml
package-name: liftr_metered_billing
package-version: "0.16.0"
azure-arm: true
```

### Ruby multi-api

``` yaml $(ruby) && $(multiapi)
batch:
  - tag: package-2018-08-31
```

### Tag: package-2018-08-31 and ruby

These settings apply only when `--tag=package-2018-08-31 --ruby` is specified on the command line.
Please also specify `--ruby-sdks-folder=<path to the root directory of your azure-sdk-for-ruby clone>`.

``` yaml $(tag) == 'package-2018-08-31' && $(ruby)
namespace: "Azure::liftrmeteredbilling::Mgmt::V2015_06_01"
output-folder: $(ruby-sdks-folder)/management/liftr_metered_billing/lib
```
