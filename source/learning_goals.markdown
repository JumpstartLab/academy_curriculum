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
* Memory requirements/usage of string creation and manipulation

###### Essential Methods

* Core Ruby
  * `chomp`
  * `strip` / `lstrip` / `rstrip`
  * `match`
  * `capitalize` / `downcase` / `upcase`
  * `each_char`
  * `empty?`
  * `start_with?` / `end_with?`
  * `gsub`
  * `delete`
  * `replace`
  * `reverse`
  * `split`
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

#### Float

* Common Methods
  * Math Operators
  * `ceil`
  * `floor`
* Formatting
  * `format("%.3f", 22.0/7)`
* Challenges when using Floats
  * Math is not precise
  * Formatting can be more difficult
* Alternatives
  * BigDecimal
  * Working without fractional components

#### Regular Expressions

### Collections

#### Array

#### Hash

#### Set

### Rails

### JavaScript

### Systems & Tooling

### Software Engineering

### Design

### Other Topics