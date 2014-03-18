##  Create doubles

    angular.module('lo.directives', [])
      .directive 'double', ->
        {
          transclude: 'element'
          priority: 2500,
          link: (scope, elem, attrs, ctrl, transclude) ->
            for num in [0, 1]
              newScope = scope.$new()
              newScope.$index = num
              transclude(newScope)
        }