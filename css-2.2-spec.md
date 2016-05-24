# CSS 2.2

* https://www.w3.org/TR/CSS22/

## 1. About the spec

normative vs non-normative

> A normative definition or statement is one that should be taken as
> authoritative or imperative (i.e., a should or a must), while a non-normative
> one is one that bears no such restriction.
>
> Synonyms for normative would include prescriptive, so synonyms of
> non-normative could range from descriptive to declarative to informal or
> casual, depending on context.
>
> http://english.stackexchange.com/questions/28882/meaning-of-non-normative

* they use single quotes to delimit
    * property name
    * pseudo-class name
    * value

## Anatomy of a property definition

* Name
    * property name
* Value
    * a BNF expression showing all legal values of the property
* initial
    * "initial value" of the property
* Applies to
    * all properties can legally be added to all elements but they don't all apply
    * e.g. `clear` only applies to block elements
* Inherited
    * whether the property is inherited from parent element or not
* Percentages
    * tells you how to interpret percentage values
* Media
    * the media groups this property belongs to
* Computed value

