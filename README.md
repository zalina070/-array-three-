# -array-three-
function joinEvenPairs(str) {
  // Разбиваем строку на массив символов (цифр)
  const digits = str.split('');
  let result = '';
  
  for (let i = 0; i < digits.length; i++) {
    result += digits[i];
    
    // Проверяем, если текущая и следующая цифра — чётные, то не ставим дефис
    if (
      i < digits.length - 1 && // не последний элемент
      +digits[i] % 2 === 0 &&  // текущая чётная
      +digits[i + 1] % 2 === 0 // следующая чётная
    ) {
      // ничего не добавляем
    } else if (i !== digits.length - 1) {
      // иначе добавляем дефис (если не последний элемент)
      result += '-';
    }
  }
  
  return result;
}

console.log(joinEvenPairs("025468")); 
 # 2
var arr1 = [-3, 8, 7, 6, 5, -4, 3, 2, 1];

// По возрастанию с учётом чисел (используем compare function)
arr1.sort((a, b) => a - b);

console.log(arr1.join(',')); // "-4,-3,1,2,3,5,6,7,8"

