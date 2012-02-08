The following list attempts to document the knowledge/skills a developer needs to be "proficient" in Ruby. It is not intended to be exhaustive, and likely many points can be debated.

## Ruby

### Classes

* Basic structure
* Writing instance methods
* Writing class methods
  * Using `self`
  * Using `class << self`
* Parameters
  * Finite
  * With Default Values
  * Named Parameters with Hashes
    * Combining with default values
* Modules
  * Basic Construction
  * Use in Namespacing
  * Used for Class Decomposition
    * Writing Instance Methods
    * Writing Class Methods
    * `include` vs `extend`
    * Using `self.included`
    * Using `ActiveSupport::Concern`
  * Testing a module
  * Method lookup chain

### Basic Objects
  
#### String

##### Concepts

* Creating / Definition
* Single vs. Double Quoted Strings
* Combining Strings and Other Data
  * Concatenation with `+`
  * Wrapping in an Array and using `join`
  * Interpolating
* Implications of UTF8 encoding and Ruby 1.9
* Implications of "Normal" and "Bang" method variants
* Differences between strings and symbols
* Memory requirements/usage of string creation and manipulation

##### Essential Methods

* Core Ruby
  * `chomp`
  * `strip`
  * `match`
  * `capitalize` / `downcase` / `upcase`
  * `each_char` / `chars`
  * `empty?`
  * `start_with?` / `end_with?`
  * `gsub`
  * `delete`
  * `replace`
  * `reverse`
  * `split`
  * `length` and `bytesize`
  * `include?`
  * `<=>`
  * `[]`
  * `<<`
  * `=~`
  * `to_i` / `to_f`
* With `ActiveSupport`
  * `titleize`
  * `camelize` / `underscore`
  * `classify`
  * `constantize`
  * `dasherize`
  * `humanize`
  * `parameterize`
  * `pluralize` / `singularize`

#### Fixnum

##### Concepts

* Numbers in Ruby are Objects
  * We can call methods on numbers
  * We can define methods on numbers

##### Essential Methods

* Core Ruby
  * Core Math Operators (`+`, `-`, `*`, `/`)
  * Modulo `%`
  * `times`
  * `to_s` / `to_f`
* With `ActiveSupport`
  * Date/Time Extensions: `.hours`, `.days`, `.weeks`, `.months`, `.years`, `.ago`/`.until`, `.since`/`.from_now`
  * Byte Extensions: `.bytes`, `.kilobytes`, `.megabytes`, `.gigabytes`
  * `ordinalize`

#### Float

##### Concepts

* Challenges when using Floats
  * Math is not precise
  * Formatting can be more difficult
* Alternatives
  * `BigDecimal`
  * Avoiding fractional components
* Using `Kernel.format`
* Whole Number Math vs. Fractional Math (ex: `1.0/2` vs `1/2`)

##### Essential Methods

* Core Ruby
  * Core Math Operators (`+`, `-`, `*`, `/`)
  * `ceil` 
  * `to_i` / `floor`
  * `to_s`  

#### Regular Expressions

#### Range

#### Date and Time

### Collections

#### Array

#### Hash

#### Enumerable

#### Set

### Rails

### JavaScript

### Systems & Tooling

### Software Engineering

### Design

### Other Topics