# TestYoSass

This is designed as a really simple way to test Sass functions for a desired output. Useful if you're making changes and have functions nested several levels deep.

### Installation
```sh
$ npm install test-yo-sass
```

### Usage
Create a test.scss file in your project and include your relevant sass functions and variables.

Then include TestYoSass and set up your tests. The below code adds a single test called 'mytest'. This is designed to compile to a CSS file (lol, not valid CSS) which outputs a log for each test. This allows you to see the value and expected value for each test, as well as a count of passing/failing tests. 

```
@import 'config/colors';
@import 'functions/map-functions';

@import '../../../../node_modules/test-yo-sass/tys';

#TestYoSass {

	mytest: _add_test( 'mytest', (
		name: 'Name of my test',
		value: yourfunctionname( 
			$functionarg 
			$foobar
		),
		expected: 'returnedvalue'
	));

	@include _run_tests();

}
```

### License 
MIT, plz hack away.