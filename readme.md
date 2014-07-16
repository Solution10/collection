# Solution10\Collection

Like Arrays. Only better!

## What does this do?

Collections, at their core, are implementations of Iterator, ArrayAccess and Countable. But they're also a lot more than that.

Splice subsections of arrays simply by passing keys:

    $collection = new Collection(array('Apple', 'Orange', 'Banana'));
    $subset = $collection['1:2'];
    // $subset is now: array('Apple', 'Orange')

    $collection = new Collection(array('Apple', 'Orange', 'Banana'));
    $subset = $collection['-2:2'];
    // $subset contains ('Orange', 'Banana')

    $collection = new Collection(array('Apple', 'Orange', 'Banana', 'Grapes'));
    $subset = $collection[':LAST'];
    // $subset is simply array('Grapes')

Quickly and easily Sort

    $collection = new Collection(array(100, 50, 70, 10));
    $collection->sort(Collection::SORT_ASC);
    // $collection's order is now: 10, 50, 70, 100

    $collection = new Collection(array(
        array(
            'name' => 'Sarah',
            'job' => 'Manager',
        ),
        array(
            'name' => 'Alex',
            'job' => 'Developer',
        ),
        array(
            'name' => 'Tracy',
            'job' => 'HR'
        ),
    ));
    $collection->sort_by_member('name', Collection::SORT_ASC);

## Installation

Install via composer:

    "require": {
        "solution10/collection": "1.*"
    }

## Requirements

- PHP >= 5.3

That's it!

## Documentation

See the [docs/ folder in the repo](http://github.com/solution10/collection/tree/master/docs).

## License

[MIT](http://github.com/solution10/collection/tree/master/LICENSE.md)

## Contributing

[Contributors Notes](http://github.com/solution10/collection/tree/master/CONTRIBUTING.md)
