
## codewars solutions

various solutions i have completed on codewars

##

## Sum of integers in string

https://www.codewars.com/kata/598f76a44f613e0e0b000026

func sumOfIntegersInString(_ string: String) -> Int {
    var sum = 0
    var currentNumber = 0
    var negative = false
    
    for char in string {
        if let intValue = Int(String(char)) {
            currentNumber = currentNumber * 10 + intValue
        } else {
            if negative {
                sum -= currentNumber
            } else {
                sum += currentNumber
            }
            currentNumber = 0
            negative = false
            if char == "-" {
                negative = true
            }
        }
    }
    
    if negative {
        sum -= currentNumber
    } else {
        sum += currentNumber
    }
    
    return sum
}

##

