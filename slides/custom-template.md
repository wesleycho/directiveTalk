##  Custom template

    angular.module('lo.directives')
      .directive 'specialSelect', -> {
        restrict: 'E'
        replace: true
        template: (element, attrs) ->
          return '<select ng-model="' + attrs.ngModel +
            '" ng-options="' + attrs.ngOptions +
            '"><option value="">' + attrs.initial + '</option>' +
            '</select>'
      }