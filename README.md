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

## Contributing

1. Fork it (<https://github.com/crystal-lang/yaml_mapping.cr/fork>)
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create a new Pull Request
