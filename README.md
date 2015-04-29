# Accessibility Specifications

It can be hard to track down correct and up to date information on how to make
a UI accessible. So I decided to create a repository of information to help me
and anyone else looking for this type of information.

It covers things like:

- What [WAI-ARIA](http://www.w3.org/WAI/intro/aria.php) to apply.
- What keyboard functionality to apply.
- Markup and in some cases CSS code examples.
- What should happen when JavaScript is disabled.
- Examples where available.

And will include components such as:

- [Accordion](components/accordion/README.md)
- Autocomplete
- Carousel
- Datepicker
- Modal
- Tabs
- Tree

*This is a living document* and feel free to create
[issues](https://github.com/chris-pearce/accessibility-specs/issues) for any
new additions or improvements, log any issues, or just ask a question, and
label appropriately. Or create a
[Pull Request](https://help.github.com/articles/using-pull-requests/).

## Contents

- [Components](components)
  - [Accordion](components/accordion/README.md)

## Noteworthy

- `x` equals any element within markup blocks.
- The following conventions are used for
  [DOM hooks](http://presentation.chris-pearce.me/DOM-hooks/):
  - [State hooks](https://github.com/chris-pearce/css-guidelines#state-hooks)
  - [JS hooks](https://github.com/chris-pearce/css-guidelines#javascript-hooks)

## Resources

- [WAI-ARIA 1.0 Authoring Practices](http://www.w3.org/TR/wai-aria-practices/)
- [WAI-ARIA 1.0 Authoring Practices -> Design Patterns](http://www.w3.org/TR/wai-aria-practices/#aria_ex)
- [Using WAI-ARIA in HTML](http://rawgit.com/w3c/aria-in-html/master/index.html)
- [Techniques for WCAG 2.0](http://www.w3.org/TR/WCAG20-TECHS/Overview.html)
- [How To Meet WCAG 2.0](http://www.w3.org/WAI/WCAG20/quickref/)
- [The Paciello Group -> Resources](http://www.paciellogroup.com/resources/)
- [WebAIM](http://webaim.org/)
- [Simply Accessible -> Articles](http://simplyaccessible.com/articles/)
- [The Accessibility Project](http://a11yproject.com/)
- [Deque Blog](http://www.deque.com/blog/)
- [Web Usability -> Articles](http://usability.com.au/category/articles/)
- [DHTML Style Guide Working Group Recommended Keyboard Shortcuts](http://access.aol.com/dhtml-style-guide-working-group/)
- [Web Accessibility Testing Techniques](http://pauljadam.com/weba11ytesting/)
- [Basic screen reader commands for accessibility testing](http://www.paciellogroup.com/blog/2015/01/basic-screen-reader-commands-for-accessibility-testing/)

## Libraries

- [Open AJAX Alliance Accessibility Tools](http://www.oaa-accessibility.org/examples/)
- [Accessible jQuery-ui Components Demonstration](http://hanshillen.github.io/jqtest/)
- [AccDC: Accelerated Dynamic Content](http://whatsock.com/)
- [Practical ARIA Examples](http://heydonworks.com/practical_aria_examples/)

## Tools

- [WAVE Toolbar](https://wave.webaim.org/toolbar/)
- [Colour Contrast Checker](http://leaverou.github.io/contrast-ratio/)
- [aViewer](http://www.paciellogroup.com/blog/2013/03/aviewer-2013/)
- [HTML_CodeSniffer](http://squizlabs.github.io/HTML_CodeSniffer/)

*Web accessibility evaluation tools can be very helpful; however, they do not replace the need for human evaluation. Evaluating for accessibility requires knowledgeable human judgment. No tool alone can determine if a site meets accessibility guidelines. (However, a tool can determine if a site does not meet accessibility guidelines.) Testing tools can increase the efficiency of evaluation. Experience with assistive technologies is required to evaluate for usable accessibility.*
