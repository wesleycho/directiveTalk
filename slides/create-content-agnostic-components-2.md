##  Create content agnostic components

### Coffeescript

    angular.module('lo.directives', [])
      .directive 'dropdownToggle', -> {
        transclude: true
        template: '<div ng-transclude></div>'
        restrict: 'ECA'
        require: 'dropdown'
        scope: {}
        controller: ($scope, $element) ->
          $scope.open = false
          this.toggle = () -> $scope.open = !$scope.open
          $element.on 'click', (e) ->
            e.preventDefault();
            e.stopPropagation();
            this.toggle();
          $scope.$watch 'open', (val) ->
            $element.sibling('.dropdown')[val ? show : hide]();
      }

