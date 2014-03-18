##  Modify input

    angular.module('lo.directives', [])
      .directive 'restrictInteger', ->
        {
          restrict: 'A'
          require: 'ngModel'
          link: (scope, elem, attrs, ctrl) ->
            ctrl.$parsers.push (input) ->
              if not _(input).isNumber() then input = +input
              input
        }