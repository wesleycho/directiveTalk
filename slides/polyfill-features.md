##  Polyfill features

### Example

    // jQuery Placeholder plugin
    if (!('placeholder' in document.createElement('input'))) {
      angular.module('ngEiQ.common.directives')
        .directive('placeholder', function () {
          return {
            restrict: 'A',
            link: function (scope, elem, attrs) {
              elem.placeholder();                   
            }
          };
        });
    }