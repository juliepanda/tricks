#### Using Subject.find_each instead of Subject.find when iterating
When looping thorugh a collection of records from the database using the `SUbject.all` method causes Ruby to pull and cache batch size of 5000mb (more than you need). Instead, use [batch processing](http://api.rubyonrails.org/classes/ActiveRecord/Batches.html).<br>
Instead of iterating with, <br>
```ruby
Material.each do |materia|
    material.do_something
end
```
Use,
```ruby
Material.find_each do |materia|
    material.do_something
end
```