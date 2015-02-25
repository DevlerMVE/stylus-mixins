# Em

```css
em($px, [$base])
```

Returns an em value, based on a passed pixel value with an optional base font-size.

```css
em($px $px $px $px, [$base])
```

Multiple pixel values can be passed to the mixin.

```css
$base--font-size ?= 16px
```
* Sets a base font size, used for calculating em values. Default value is provided.
* Use this variable within a project to set a custom value.

```css
@param $px
  type: unit (pixel)
```
* A pixel value passed to this mixin will be converted to an em value.

```css
@param $base
  type: unit (pixel)
  default: $base--font-size
```
* Custom base values can be used if required to override the default base font-size.

---

**Example – single value**
```css
.element
  font-size em(32) // 32/16 = 2

/* CSS */
.element {
  font-size: 2em;
}
```

**Example - multiple values**

```css
.element
  margin em(16 32) // 16/16 = 1, 32/16 = 2

/* CSS */
.element {
  margin: 1em 2em;
}
```

**Example - custom base font size**

```css
.element
  margin em(16 32, 32) // 16/32 = 0.5, 32/32 = 1

/* CSS */
.element {
  margin: 0.5em 1em;
}
```



---

[Source](https://github.com/jackbrewer/stylus-mixins/blob/master/lib/stylus-mixins/units/em.styl) - [Tests](https://github.com/jackbrewer/stylus-mixins/blob/master/test/tests/units/em.styl)
