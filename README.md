# This || that

This repo is meant to act as a collection of resources describing similar
methods, classes, patterns or techniques in Ruby and Rails. These entities might
be similar in name, functionality or usage but have some differences that may or
may not be readily apparent.

The provided resources largely differences in usage and semantics and might not
include differences in performance or version compatibility.

When reading the resources, consider any accepted answers and discussion and
note that some information might be more or less relevant for different versions
of Ruby or Rails.

This is a work in progress and is not expected to be exhaustive. If you have any
suggestions, additions, clarifications or corrections, please feel free to open
an issue or a pull request.

NOTE: aliases, such as `update` and `update_attributes` from ActiveRecord, are
not included in this list.

For more information, see [the slides from the talk at RailsConf
2024](https://docs.google.com/presentation/d/1-IATp3rDmctTlXqDDdCLssMc_dl8j4MdIF5TV063EU0/edit?usp=sharing)
(video will be added once available).

To see a searchable table of contents, click the list button on GitHub visible here:

![image](https://github.com/andycandrea/this_or_that.rb/assets/5621517/4f165a3c-d63a-4657-aace-7328ee045dcc)

## `.new` vs `#initialize`

* [The difference between initialize and self.new](https://stackoverflow.com/questions/24130457/the-difference-between-initialize-and-self-new)

## `<<` vs `push` vs `concat`

* [Ruby - Difference between Array#<< and Array#push](https://stackoverflow.com/questions/10569529/ruby-difference-between-array-and-arraypush)

## `==` vs `===` vs `eq?` vs `equal?`

* [ruby - What's the difference between equal?, eql?, ===, and ==?](https://stackoverflow.com/questions/7156955/whats-the-difference-between-equal-eql-and)
* RSpec matchers
  * `==:` `eq`
  * `===:` None
  * `eql?`: `eql`
  * `equal?`: `equal`

## `Array#[1]`/`Array#[-1]` vs `Array#first`/`Array#last`

* [FastRuby repo](https://github.com/fastruby/fast-ruby?tab=readme-ov-file#array0-vs-arrayfirst-code)
* [Ruby convention for accessing first/last element in array [closed]](https://stackoverflow.com/questions/18212240/ruby-convention-for-accessing-first-last-element-in-array)

## Backticks vs `system` vs `exec` vs `fork` vs `IO.popen` vs `Open3.popen3` vs `PTY.spawn`

* [Ruby, Difference between exec, system and %x() or Backticks](https://stackoverflow.com/questions/6338908/ruby-difference-between-exec-system-and-x-or-backticks)
* Note: you can use backticks with a heredoc in order to execute long/multi-line
  statements. See [the
  docs](https://docs.ruby-lang.org/en/master/syntax/literals_rdoc.html#label-Here+Document+Literals)

## Blocks vs procs vs lambdas

* [Understanding Ruby - Blocks, Procs, and Lambdas](https://dev.to/baweaver/understanding-ruby-blocks-procs-and-lambdas-24o0)

## Class vs instance methods

* [Unraveling Classes, Instances and Metaclasses in Ruby](https://blog.appsignal.com/2019/02/05/ruby-magic-classes-instances-and-metaclasses.html)

## `Hash#[]` vs `fetch` vs `dig`

* [ruby - fetch vs. [] when working with hashes?](https://stackoverflow.com/questions/16569409/fetch-vs-when-working-with-hashes)
* [ruby on rails - Could someone explain me what is the difference between Hash#dig vs Hash#fetch](https://stackoverflow.com/questions/55429632/could-someone-explain-me-what-is-the-difference-between-hashdig-vs-hashfetch)

## `Hash.new(default)` vs `Hash.new { default }`

* [What's the difference between "Hash.new(0)" and "{}" - Stack Overflow](https://stackoverflow.com/questions/35177845/whats-the-difference-between-hash-new0-and)
* [A trick with Ruby Hash.new - DEV Community](https://dev.to/factorial/a-trick-with-ruby-hash-new-2ma0)
* [Ruby hash default value behavior - Stack Overflow](https://stackoverflow.com/questions/16159370/ruby-hash-default-value-behavior)
* [Ruby Hash.new with a block need in-depth explanation - Stack Overflow](https://stackoverflow.com/questions/59869743/ruby-hash-new-with-a-block-need-in-depth-explanation)

## `Kernel#Array` vs `Array.new` vs `[]`

* [Why Array.new(3, []) works differently than [[], [], []] in Ruby?](https://stackoverflow.com/questions/42615737/why-array-new3-works-differently-than-in-ruby)
* [Ruby array creation, Array.new vs []](https://stackoverflow.com/questions/4601652/ruby-array-creation-array-new-vs)
* `Array()` is shorthand for [`Kernel.Array`](https://ruby-doc.org/3.3.0/Kernel.html#method-i-Array) implicitly

## `Kernel#format` vs `Float#round().to_s`

* [Rounding float in Ruby - Stack Overflow](https://stackoverflow.com/questions/2054217/rounding-float-in-ruby)
  * See discussion in accepted answer for distinction

## Long vs short coercion

* [to_s vs. to_str (and to_i/to_a/to_h vs. to_int/to_ary/to_hash) in Ruby - Stack Overflow](https://stackoverflow.com/questions/11182052/to-s-vs-to-str-and-to-i-to-a-to-h-vs-to-int-to-ary-to-hash-in-ruby)

## Normal vs dashed vs squiggly heredocs

* [Heredocs and how to use them in Ruby and Rails | Saeloun Blog](https://blog.saeloun.com/2020/04/08/heredoc-in-ruby-and-rails/)
* Additional heredoc info
  * [Weird Ruby: Heredoc Delimiters | Meta Redux](https://metaredux.com/posts/2022/01/20/weird-ruby-heredoc-delimiters.html)

## `Object` vs `BasicObject`

* [What's the difference between Object and BasicObject in Ruby? - Stack Overflow](https://stackoverflow.com/questions/8894817/whats-the-difference-between-object-and-basicobject-in-ruby)

## Path helpers vs URL helpers

* [Named routes _path vs _url - ruby on rails](https://stackoverflow.com/questions/11939865/named-routes-path-vs-url)

## Positional vs arg-based privacy

* [How to define a private method in Ruby? - Stack Overflow](https://stackoverflow.com/questions/22029396/how-to-define-a-private-method-in-ruby)
  * Note the inline option available since Ruby 2.1
* Note that positional privatization does not affect class methods
  * Doing a `def self.method` after a `private` will *not* make it a private
    class method

## Refinements vs monkey-patching

* [Mastering Refinements in Ruby: A Comprehensive Guide to Safer Monkey
    Patching: part 1 | by Talaat Magdy](https://talaatmagdyx.medium.com/mastering-refinements-in-ruby-a-comprehensive-guide-to-safer-monkey-patching-531dfdb86608)

## `''` vs `""` vs `String.new` vs `Kernel.String`

* Single-quoted behavior in heredocs
  * [Weird Ruby: Single-quoted Heredocs | Meta Redux](https://metaredux.com/posts/2019/05/22/weird-ruby-single-quoted-heredocs.html)
* [What's the difference between String.new and a string literal in Ruby? - Stack Overflow](https://stackoverflow.com/questions/41602998/whats-the-difference-between-string-new-and-a-string-literal-in-ruby)
* [Double vs single quotes - Stack Overflow](https://stackoverflow.com/questions/6395288/double-vs-single-quotes)
* `#frozen_string_literal: true`
  * Respected by literals and `String()`
  * Not respected by `String.new`
* Note: you can also declare single-character strings using the [single
    character literal
    syntax](https://docs.ruby-lang.org/en/master/syntax/literals_rdoc.html#label-String+Literals)

## `Struct` vs `OpenStruct` vs `Data`

* `Struct` vs `OpenStruct`
  * [When should I use Struct vs. OpenStruct? - Stack Overflow](https://stackoverflow.com/questions/1177594/when-should-i-use-struct-vs-openstruct)
* `Struct` vs `Data`
  * [Ruby 3.2 introduces Data, a new core class for immutable value objects | Shakacode](https://www.shakacode.com/blog/ruby-3-2-adds-a-new-data-class/)

## `Time` vs `DateTime` vs `ActiveSupport::TimeWithZone`

* Note that differences have changed over time
* [class DateTime - Documentation for Ruby 3.4](https://docs.ruby-lang.org/en/master/DateTime.html#class-DateTime-label-When+should+you+use+DateTime+and+when+should+you+use+Time-3F)
* [ActiveSupport::TimeWithZone](https://api.rubyonrails.org/classes/ActiveSupport/TimeWithZone.html)
* See also:
  * [`acts_like?`](https://api.rubyonrails.org/classes/Object.html#method-i-acts_like-3F)
  * [`Date#acts_like_date?`](https://api.rubyonrails.org/classes/Date.html#method-i-acts_like_date-3F)
    and [`DateTime#acts_like_date?`](https://api.rubyonrails.org/classes/DateTime.html#method-i-acts_like_date-3F)
  * [`Time#acts_like_time?`](https://api.rubyonrails.org/classes/Time.html#method-i-acts_like_time-3F),
  * [`DateTime#acts_like_time?`](https://api.rubyonrails.org/classes/DateTime.html#method-i-acts_like_time-3F),
  * [`TimeWithZone#acts_like_time?`](https://api.rubyonrails.org/classes/ActiveSupport/TimeWithZone.html#method-i-acts_like_time-3F)

## `a + b` vs `b + a`

* Methods (including mathematical operations) are not inherently commutative in
  Ruby
* `a + b` is equivalent to `a.+(b)`; if `a` and `b` are different classes, a
  different underlying method will likely be called when swapping the order
* Examples
  * `===`
    * `String === ""` vs `"" === String`
    * `/string/ === "string"` vs `"string" === /string/`
    * `(1..5) === 3` vs `3 === (1..5)`
  * `*`
    * `"a" * 3` vs `3 * "a"`
  * `+`
    * `Time.zone.now + 1.day` vs `1.day + Time.zone.now`

## `a ||= b` vs `a || a = b` vs `a = a || b`

* [What does ||= (or-equals) mean in Ruby? - Stack Overflow](https://stackoverflow.com/questions/995593/what-does-or-equals-mean-in-ruby)

## `alias` vs `alias_method`

* [ruby - Should I use alias or alias_method? - Stack Overflow](https://stackoverflow.com/questions/4763121/should-i-use-alias-or-alias-method)

## `ancestors.include?` vs `Module#<=` vs `Module#<`

* [Module#< docs](https://ruby-doc.org/3.3.0/Module.html#method-i-3C)
* [Module#<= docs](https://ruby-doc.org/3.3.0/Module.html#method-i-3C-3D)
* [Module#ancestors docs](https://ruby-doc.org/3.3.0/Module.html#method-i-ancestors)
  * More similar to `<=`, but see
    [fast-ruby](https://github.com/fastruby/fast-ruby?tab=readme-ov-file#ancestorsinclude-vs--code)

## `any?` vs `count > 0` vs `exist?`

* [Faster Rails: How to Check if a Record Exists - Semaphore](https://semaphoreci.com/blog/2017/03/14/faster-rails-how-to-check-if-a-record-exists.html)

## `as_json` vs `to_json`

* [Difference between as_json and to_json method in Ruby - Stack Overflow](https://stackoverflow.com/questions/38301957/difference-between-as-json-and-to-json-method-in-ruby)

## `attr_accessor` vs `mattr_accessor` vs `cattr_accessor` vs `attr_internal_accessor`

* [What is mattr_accessor in a Rails module? - Stack Overflow](https://stackoverflow.com/questions/185573/what-is-mattr-accessor-in-a-rails-module)

## `bsearch` vs `find`

* [Binary Searching and Ruby's bsearch Method | Hashrocket](https://hashrocket.com/blog/posts/binary-searching-and-ruby-s-bsearch-method)
* [Effective Use of Array#bsearch | Jemma Issroff](https://jemma.dev/blog/array-bsearch)

## `casecmp` vs `casecmp?` vs `downcase ==`

* [How to compare strings ignoring the case - ruby](https://stackoverflow.com/questions/2844507/how-to-compare-strings-ignoring-the-case)

## `clone` vs `dup`

* [What's the difference between Ruby's dup and clone methods? - Stack
    Overflow](https://stackoverflow.com/questions/10183370/whats-the-difference-between-rubys-dup-and-clone-methods)

## `count` vs `length` vs `size`

* For Ruby
  * [ruby - What is the difference between `size` and `length` methods - Stack Overflow](https://stackoverflow.com/questions/35816739/what-is-the-difference-between-size-and-length-methods)
* For Rails
  * [Ruby on Rails: length vs size vs count with examples | by Gonzalo Galdámez | Unagi | Medium](https://medium.com/unagi/ruby-on-rails-length-vs-size-vs-count-with-examples-a32e17274c79)

## `defined?(yield)` vs `block_given?`

* [The defined? keyword in Ruby](https://medium.com/rubycademy/the-defined-keyword-in-ruby-b7a5a5a48e1e)

## `delete_suffix` vs `chomp`

* [`chomp` docs](https://ruby-doc.org/3.3.0/String.html#method-i-chomp)
  * Additional complexity over delete_suffix
  * Has existed for much longer
* [`delete_suffix` docs](https://ruby-doc.org/3.3.0/String.html#method-i-delete_suffix)
  * Not introduced until Ruby 2.5

## `distinct` vs `uniq`

* [Rails: uniq vs. distinct - Stack Overflow](https://stackoverflow.com/questions/39575398/rails-uniq-vs-distinct)

## `downcase` vs `downcase!`

* [About bang methods in Ruby, from its creator | thoughtful](https://thoughtfulapps.com/articles/ruby/about-ruby-bang-methods)
* [How to convert a string to lower or upper case in Ruby - Stack Overflow](https://stackoverflow.com/questions/1020568/how-to-convert-a-string-to-lower-or-upper-case-in-ruby)
  * Comment about `downcase!` sometimes returning `nil` is important; don't
    chain bang method calls
* Both sources are pretty generalizable to bang vs non-bang methods in Ruby
  (e.g. not just `downcase`/`downcase!`)

## `each` vs `find_each` vs `find_in_batches` vs `in_batches`

* [Active Record Query Interface](https://guides.rubyonrails.org/active_record_querying.html#retrieving-multiple-objects-in-batches)
* [Rails — find_each v.s find_in_batches v.s in_batches | by 涓 / Lynn Chang | Lynn's dev blog | Medium](https://medium.com/lynns-dev-blog/rails-find-each-v-s-find-in-batches-v-s-in-batches-d5ca9bfe37d)

## `each { render ... }` vs `render ..., collection: ...`

* [Rendering Collections in Rails](https://thoughtbot.com/blog/rendering-collections-in-rails)
* [Rails 4: why is one way of rendering partials so much faster? - Stack Overflow](https://stackoverflow.com/questions/44509928/rails-4-why-is-one-way-of-rendering-partials-so-much-faster)

## `each_with_object` vs `reduce(:to_h)`

* [each_with_object vs. reduce/inject](https://www.leejroberts.com/reduce-vs-each_with_object/)

## `f.select` vs `select_tag`

* [ActionView::Helpers::FormTagHelper](https://api.rubyonrails.org/v7.1.3.2/classes/ActionView/Helpers/FormTagHelper.html)
* [ActionView::Helpers::FormHelper](https://api.rubyonrails.org/v7.1.3.2/classes/ActionView/Helpers/FormHelper.html)

## `flash` vs `flash.now`

* [How to Use Flash Messages in Rails - RubyGuides](https://www.rubyguides.com/2019/11/rails-flash-messages/)

## `flat_map` vs `map.flatten`

* [Fun with flat_map (in Ruby) | Software and Systems—Keith Kim](https://blog.keithkim.org/code-patterns/fun-with-flatmap)

## `form_for` vs `form_tag` vs `form_with`

* [Rails 5: form_for vs form_with - Stack Overflow](https://stackoverflow.com/questions/43868976/rails-5-form-for-vs-form-with)
* [Rails: form_with vs. form_for vs. form_tag | by Scott Espinosa](https://scottespinosa.medium.com/rails-form-with-vs-form-for-vs-form-tag-c7d94d4e1c5d)

## `group_by` vs `index_by` vs `index_with`

* [What's the purpose of index_by over group_by? - Rails - Ruby-Forum](https://www.ruby-forum.com/t/whats-the-purpose-of-index-by-over-group-by/104054)
* [Enumerable#index_with](https://api.rubyonrails.org/classes/Enumerable.html#method-i-index_with)

## `has_one|many through:` vs delegated associations

* Depending on how you use `includes` (or alternatives) and the association read
  method, either `has_many :foos, through: :bar` or `delegate :foos, to: :bar`
  could lead to unnecessary extra queries or n+1s
* Try to get your team on board with a default so that there are shared patterns
  to help the team avoid unnecessary queries

## `include` vs `extend` vs `prepend`

* [Include, Extend, And Prepend In Ruby](https://veerpalbrar.github.io/blog/2021/11/26/Include,-Extend,-and-Prepend-In-Ruby)

## `includes` vs `preload` vs `eager_load`

* [A Visual Guide to Using :includes in Rails](https://engineering.gusto.com/a-visual-guide-to-using-includes-in-rails/)

## `insert` vs `unshift`

* [What Does Ruby's Array#shift do? - Stack Overflow](https://stackoverflow.com/questions/3718625/what-does-rubys-arrayshift-do)
* [Quick reference for ruby array methods: push/pop vs. shift/unshift - DEV Community](https://dev.to/ddhogan/quick-reference-for-array-methods-pushpop-vs-shiftunshift-4g7h)

## `instance_eval` vs `class_eval` vs `eval`

* [The Difference Between `instance_eval` and `class_eval` In Ruby](https://hayford.dev/the-difference-between-instance-eval-and-class-eval-in-ruby/)
* [How to understand the difference between class_eval() and instance_eval()? - Stack Overflow](https://stackoverflow.com/questions/900419/how-to-understand-the-difference-between-class-eval-and-instance-eval)
* [Evaluation Options in Ruby - InfoQ](https://www.infoq.com/articles/eval-options-in-ruby/)

## `instance_variable_set` vs `local_variable_set`

* instance_variable_set *can* be used to define new instance variables
* local_variable_set *cannot* be used to define new local variables (except on a
  specific binding object)
  * [How to dynamically create a local variable? - ruby](https://stackoverflow.com/questions/18552891/how-to-dynamically-create-a-local-variable)

## `is_a?` vs `kind_of?` vs `instance_of?`

* [Ruby: kind_of? vs. instance_of? vs. is_a? - Stack Overflow](https://stackoverflow.com/questions/3893278/ruby-kind-of-vs-instance-of-vs-is-a)

## `local_variables` vs `defined?`

* [How to list local-variables in Ruby? - Stack Overflow](https://stackoverflow.com/questions/4487326/how-to-list-local-variables-in-ruby)

## `loop` vs `while true`

* [fast-ruby](https://github.com/fastruby/fast-ruby?tab=readme-ov-file#loop-vs-while-true-code)
* [Is there a "do ... while" loop in Ruby? - Stack Overflow](https://stackoverflow.com/questions/136793/is-there-a-do-while-loop-in-ruby)

## `merge` vs `deep_merge`

* [Merge and Deep Merge — and Why One Day You'll Find The Latter Useful | by
    Chris Waters | Medium](https://medium.com/@christhesoul/merge-and-deep-merge-and-why-one-day-youll-find-the-latter-useful-fd43f94c1226)

## `merge` vs `reverse_merge` vs `**` vs `merge!` vs `store` vs `update`

* `**hash` will give a warning if overwriting an existing key
  `warning: key :your_key is duplicated and overwritten on line n`
* [what is difference between store vs merge in ruby hashes? - Stack Overflow](https://stackoverflow.com/questions/29004428/what-is-difference-between-store-vs-merge-in-ruby-hashes)
* [Ruby Quicktips - Merge or reverse_merge a Hash](https://rubyquicktips.com/post/5186906190/merge-or-reversemerge-a-hash)
* [Ruby Double Splat Operator: A Comprehensive Cheatsheet](https://jetrockets.com/blog/ruby-double-splat-operator-cheatsheet)

## `or` vs `||`

* [Difference between "or" and || in Ruby? [duplicate]](https://stackoverflow.com/questions/2083112/difference-between-or-and-in-ruby)

## `private` vs `protected`

* [What are the differences between "private", "public", and "protected
    methods"? - Stack Overflow](https://stackoverflow.com/questions/9882754/what-are-the-differences-between-private-public-and-protected-methods)

## `respond_to?` vs `defined?` vs `method_defined?`

* ['respond_to?' versus 'defined?' - ruby](https://stackoverflow.com/questions/44107544/respond-to-versus-defined)

## `select` vs `collection_select`

* [rails collection_select vs. select - Stack
    Overflow](https://stackoverflow.com/questions/1728593/rails-collection-select-vs-select)
* Extra caveat
  * `collection_select` will do a `SELECT *` unless you tell it otherwise and
    will hydrate entire ActiveRecord model objects for each row if you do
    something like:

    ```rb
    collection_select(..., ..., Author.all, :id, :name)
    ```

  * If you don't already have everything in memory or don't need to reuse the
    collection, you'll likely get some performance improvements if you instead
    use `select` like:

    ```rb
    select(..., options_for_select(Author.pluck(:name, :id))
    ```

  * This does a `SELECT name, id` and doesn't build the entire models up in
    memory.
  * As always, do what feels right in the context of your app/team unless you
    really need every last bit of performance

## `select` vs `pluck`

* [ActiveRecord's Select & Pluck. Column Down | by Andrew Livingston |
    Medium](https://medium.com/@amliving/activerecords-select-pluck-3d5c58872053)

## `sort` vs `sort_by` vs `order`

* `order` comes from Rails and is used for constructing queries
* [Method of the Month 1: Ruby's sort vs. sort_by | Brandon Dimcheff](https://brandon.dimcheff.com/2009/11/18/rubys-sort-vs-sort-by/)
* `sort.reverse` vs `sort_by` performance:
  * [FastRuby repo](https://github.com/fastruby/fast-ruby?tab=readme-ov-file#arraysortreverse-vs-arraysort_by---block-code)

## `start_with?` vs `end_with?` vs `[0]==` vs `[-1]==`

* [fast-ruby](https://github.com/fastruby/fast-ruby?tab=readme-ov-file#stringstart_with-vs-string-code)
* [How do I find if a string starts with another string in Ruby? - Stack
    Overflow](https://stackoverflow.com/questions/4168543/how-do-i-find-if-a-string-starts-with-another-string-in-ruby)
* Also consider readability

## `tag` vs `content_tag`

* [Rails content_tag vs tag - Stack Overflow](https://stackoverflow.com/questions/20363506/rails-content-tag-vs-tag)

## `to_i` vs `Integer()`

* [ruby - Difference between Integer(value) and value.to_i - Stack Overflow](https://stackoverflow.com/questions/10093493/difference-between-integervalue-and-value-to-i)

## `to_s` vs `inspect`

* [Why do this Ruby object have both to_s and inspect methods that appear to do the same thing? - Stack Overflow](https://stackoverflow.com/questions/2625667/why-do-this-ruby-object-have-both-to-s-and-inspect-methods-that-appear-to-do-the)
* [Inspecting Ruby's inspect method](https://thoughtbot.com/blog/ruby-inspect-tutorial)

## `tr`/`tr!` vs `sub`/`sub!` vs `gsub`/`gsub!`

* [What is the difference between tr and gsub? - ruby](https://stackoverflow.com/questions/26749065/what-is-the-difference-between-tr-and-gsub)
* [What is the difference between gsub and sub methods for Ruby Strings - Stack Overflow](https://stackoverflow.com/questions/6766878/what-is-the-difference-between-gsub-and-sub-methods-for-ruby-strings)

## `try` vs `&.`

* [What is the difference between `try` and `&.` (safe navigation operator) in Ruby - Stack Overflow](https://stackoverflow.com/questions/45825363/what-is-the-difference-between-try-and-safe-navigation-operator-in-ruby)

## `update` vs `update!`

* [update! docs](https://api.rubyonrails.org/classes/ActiveRecord/Persistence.html#method-i-update-21)

## `update` vs `update_attribute` vs `update_all` vs `update_columns` vs `toggle` vs `touch` vs …

* [rubocop-rails SkipsModelValidations](https://github.com/rubocop/rubocop-rails/blob/master/lib/rubocop/cop/rails/skips_model_validations.rb)
* [ActiveRecord Validations: Skipping validations](https://guides.rubyonrails.org/active_record_validations.html#skipping-validations)
* [ActiveRecord::Persistence docs](https://api.rubyonrails.org/classes/ActiveRecord/Persistence.html#method-i-update)

## Threads vs Fibers

* [Meet Fiber, Thread's Cooperative Cousin](https://thoughtbot.com/blog/meet-fiber-thread-s-cooperative-cousin)

## `Range#cover?` vs `Range#include?`

* [This || That slides](https://docs.google.com/presentation/d/1-IATp3rDmctTlXqDDdCLssMc_dl8j4MdIF5TV063EU0/edit#slide=id.g2cd56913015_0_95)
* [Range#include? vs. Range#cover?](https://hashrocket.com/blog/posts/range-include-vs-range-cover)

## `=~` vs `match` vs `match?` vs `Regexp#===` vs `String#scan`

* [This || That slides](https://docs.google.com/presentation/d/1-IATp3rDmctTlXqDDdCLssMc_dl8j4MdIF5TV063EU0/edit#slide=id.g2cd56913015_0_100)
* [Using Match vs. =~ in Ruby](https://hashrocket.com/blog/posts/using-match-vs-equals-tilde-in-ruby)
* [Fastest way to check if a string matches a regexp in ruby?](https://stackoverflow.com/questions/11887145/fastest-way-to-check-if-a-string-matches-a-regexp-in-ruby)

## `NoMethodError` vs `NotImplementedError`

* [This || That slides](https://docs.google.com/presentation/d/1-IATp3rDmctTlXqDDdCLssMc_dl8j4MdIF5TV063EU0/edit#slide=id.g2ce54aa32c0_0_5)
* [Abstract methods and NotImplementedError in Ruby](https://nithinbekal.com/posts/abstract-methods-notimplementederror-ruby/)

## Monkey-patching vs `define_method` vs `class_eval`

* [This || That slides](https://docs.google.com/presentation/d/1-IATp3rDmctTlXqDDdCLssMc_dl8j4MdIF5TV063EU0/edit#slide=id.g2ce54aa32c0_2_26)
* [Recommended approach to monkey patching a class in ruby](https://stackoverflow.com/questions/10337712/recommended-approach-to-monkey-patching-a-class-in-ruby)
* [monkey patching vs class_eval?](https://stackoverflow.com/questions/9399358/monkey-patching-vs-class-eval)
* Warning: non-HTTPS link: [Class_eval vs Define_method](http://www.brianmehrman.com/blog/2017/04/26/class-eval-vs-define-method/)
* [Ruby's def and instance_eval vs. class_eval](https://stackoverflow.com/questions/4409023/rubys-def-and-instance-eval-vs-class-eval)

## `delegate` vs `def_delegator` vs `def_delegators` vs `SimpleDelegator` vs `DelegateClass` vs `method_missing`

* [This || That slides](https://docs.google.com/presentation/d/1-IATp3rDmctTlXqDDdCLssMc_dl8j4MdIF5TV063EU0/edit#slide=id.g2cd56913015_0_174)
* [Delegating things in Ruby](https://rubyhero.dev/delegator-design-pattern)
* [Delegate vs Forwardable vs SimpleDelegator — Ruby vs Rails](https://medium.com/@rajputlakhveer/delegate-vs-forwardable-vs-simpledelegator-ruby-vs-rails-7993106ad175)

## Various ways to call a method

* [This || That slides](https://docs.google.com/presentation/d/1-IATp3rDmctTlXqDDdCLssMc_dl8j4MdIF5TV063EU0/edit#slide=id.g2ce54aa32c0_2_30)
