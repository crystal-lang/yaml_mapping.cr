# yaml_mapping

Provides the legacy `YAML.mapping` macro method.

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

1. Fork it (<https://github.com/your-github-user/yaml_mapping.cr/fork>)
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create a new Pull Request
