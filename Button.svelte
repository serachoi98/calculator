<script>
    export /**
* @type {any}
*/
     let key;
    export /**
* @type {string}
*/
     let result;
    const error = "Invalid input!";
    
    /**
* @param {string} value
*/
    function replace(value) {
        return value.replace("x", "*").replace("÷", "/");
    }
    function handleClick() {
        switch (key) {
            case "=":
                try {
                    result = eval(replace(result));
                } catch (e) {
                  result = error;
                }
                break;
            case "C":
                result = "0"
                break;
            default:
                result= result === error || result === "0" ? key : result + key;
        }
    }
</script>


<style>
    button {
       width: 80px;
       height: 80px;
       display: flex;
       align-items: center;
       justify-content: center;
       font-size: 24px;
       background-color: teal;
       }
    </style>

<button on:click={handleClick}>{key}</button>