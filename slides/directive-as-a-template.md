## Directive as a Template

### JS

    angular.module('lo.directives')
        .directive 'loadingSpinner', -> {
            templateUrl: 'bower_components/lo-angular-library/src/js/directives/loadingSpinner/loadingSpinner.html'
            restrict: 'E'
        }