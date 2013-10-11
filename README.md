# perl-bundles

To speed up certain Perl projects build time, it is a good idea to have a
common set of modules bundled into a single package and have it included during build and runtime.

So basically each directory in root of this repo has a `debian/` directory
which lists a set of instructions how to build a specific pacakge. For example,
`perl-catalyst-bundle` bundles `Catalyst` framework and its dependencies into a
single package using `Task::Catalyst`.

We use a simple jenkins job which clones this repo, cds into one of the
directories and build a package.
