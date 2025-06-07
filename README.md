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

// Пример:
console.log(joinEvenPairs("025468")); // "0-254-6-8"
