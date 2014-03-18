##  Directive as a Template

### CSS

    loading-spinner {
        position:relative;
        width:64px;
        height:80px;
        display:block;

        div {
            position:absolute;
            background-color:@color_primary_light;
            width:10px;
            height:25px;
            border-radius:9px 9px 0 0;
            transform:scale(0.4);
            animation-name:fadeG;
            animation-duration:1.04s;
            animation-iteration-count:infinite;
            animation-direction:linear;
        }

        div:nth-of-type(1) {
            left: 0;
            top: 29px;
            animation-delay: 0.39s;
            transform: rotate(-90deg);
        }
        div:nth-of-type(2) {
            left: 8px;
            top: 10px;
            animation-delay: 0.52s;
            transform: rotate(-45deg);
        }
        div:nth-of-type(3) {
            left: 27px;
            top: 3px;
            animation-delay: 0.65s;
            transform: rotate(0deg);
        }
        div:nth-of-type(4) {
            right: 8px;
            top: 10px;
            animation-delay: 0.78s;
            transform: rotate(45deg);
        }
        div:nth-of-type(5) {
            right: 0;
            top: 29px;
            animation-delay: 0.9099999999999999s;
            transform: rotate(90deg);
        }
        div:nth-of-type(6) {
            right: 8px;
            bottom: 7px;
            animation-delay: 1.04s;
            transform: rotate(135deg);
        }
        div:nth-of-type(7) {
            bottom: 0;
            left: 27px;
            animation-delay: 1.1700000000000002s;
            transform: rotate(180deg);
        }
        div:nth-of-type(8) {
            left: 8px;
            bottom: 7px;
            animation-delay: 1.3s;
            transform: rotate(-135deg);
        }

        @-moz-keyframes fadeG {
          0% {
            background-color:@color_primary
          }
          100% {
            background-color:@color_primary_light
          }
        }

        @-webkit-keyframes fadeG {
          0% {
            background-color:@color_primary
          }
          100% {
            background-color:@color_primary_light
          }
        }

        @-ms-keyframes fadeG {
          0% {
            background-color:@color_primary
          }
          100% {
            background-color:@color_primary_light
          }
        }

        @-o-keyframes fadeG {
          0% {
            background-color:@color_primary
          }
          100% {
            background-color:@color_primary_light
          }
        }
         @keyframes fadeG {
          0% {
          background-color:@color_primary
          }
           100% {
          background-color:@color_primary_light
          }
        }
    }
