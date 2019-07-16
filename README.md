# recipeingredients

<img src="https://img.shields.io/badge/coverage-75%25-brightgreen.svg?style=flat-square" alt="Code coverage">&nbsp;<a href="https://travis-ci.org/schollz/recipeingredients"><img src="https://img.shields.io/travis/schollz/recipeingredients.svg?style=flat-square" alt="Build Status"></a>&nbsp;<a href="https://godoc.org/github.com/schollz/recipeingredients"><img src="http://img.shields.io/badge/godoc-reference-5272B4.svg?style=flat-square" alt="Go Doc"></a> 

This is a Golang library for *ingredient tagging* and *extraction* from culinary recipes made to be used on **any site on the internet**. This library compartmentalizes and improve aspects of recipe extraction that I did previously with [schollz/meanrecipe](https://github.com/schollz/meanrecipe) and [schollz/extract_recipe](https://github.com/schollz/extract_recipe). 

## Usage

You can use as a library.

```
$ go get github.com/schollz/recipeingredients
```

Pick a random website, like [JoyFoodSunshine](https://joyfoodsunshine.com/the-most-amazing-chocolate-chip-cookies/), and you can extract the ingredients:

```go
r, _ := recipeingredients.NewFromURL("https://joyfoodsunshine.com/the-most-amazing-chocolate-chip-cookies/")
r.Parse()
fmt.Println(r.PrintIngredientList())
// Output:
// 1 cup butter (salted)
// 1 cup sugar (white)
// 1 cup brown sugar (light)
// 2 tsp vanilla (pure)
// 2 whole eggs
// 3 cups flour (all purpose)
// 1 tsp baking soda
// 1/2 tsp baking powder
// 1 tsp salt (sea)
// 2 cups chocolate chips
```

Please make an issue if you find a problem.

## How does it work?

See my blog post about it: [schollz.com/blog/ingredients](https://schollz.com/blog/ingredients).

## Develop

If you modify the `corpus/` information then you will need to run 

```
$ go generate
```

before using the library again.

## Contributing

Pull requests are welcome. Feel free to...

- Revise documentation
- Add new features
- Fix bugs
- Suggest improvements

## License

MIT
