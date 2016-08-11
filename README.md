# Testing module data with hiera

Do the following:

~~~
git clone git@github.com:thrnio/module_hiera_test.git
puppet apply --modulepath=. -e 'include ::module_hiera_test, ::module_hiera_test::foo'
~~~

You should see the output:

~~~
Notice: Scope(Class[Module_hiera_test]): module_hiera_test::foobar: banana
Notice: Scope(Class[Module_hiera_test::Foo]): module_hiera_test::foo::bar: apple
Notice: Compiled catalog for rafiki.corp.puppetlabs.net in environment production in 0.22 seconds
Notice: Applied catalog in 0.04 seconds
~~~
