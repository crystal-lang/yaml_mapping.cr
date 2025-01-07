> [!IMPORTANT]
> This library is no longer supported or updated by the Crystal Team,
> therefore we have archived the repository.
> 
> The contents are still available readonly and continue to work as a
> [shards](https://github.com/crystal-lang/shards/) dependency.
>
> If you wish to continue development yourself, we recommend you fork it.
> We can also arrange to transfer ownership.
>
> If you have further questions, please reach out on on https://forum.crystal-lang.org
> or crystal@manas.tech

# yaml_mapping

Provides the legacy `YAML.mapping` macro method.

This shard is provided as-is and considered deprecated. It won't receive feature enhancements.

Please consider using [`YAML::Serializable`](https://crystal-lang.org/api/latest/YAML/Serializable.html) instead, the successor included in Crystal's standard library.

## Installation

1. Add the dependency to your `shard.yml`:

   ```yaml
   dependencies:
     yaml_mapping:
       github: crystal-lang/yaml_mapping.cr
   ```

2. Run `shards install`

## Usage

```crystal
require "yaml_mapping"

class Employee
  YAML.mapping(
    title: String,
    name: String,
  )
end

employee = Employee.from_yaml("title: Manager\nname: John")
employee.title # => "Manager"
employee.name  # => "John"

employee.name = "Jenny"
employee.name # => "Jenny"
```
