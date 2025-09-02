# HackerRank_2lista *Segunda Lista*

## 📌- Angry Professor 

<pre>
function angryProfessor(k, a) {
    const onTimeCount = a.filter(time => time <= 0).length;

    return onTimeCount < k ? "YES" : "NO";
}

</pre>

## 📌2- Cats and a Mouse 

<pre>
function catAndMouse(x, y, z) {
    const distA = Math.abs(x - z);
    const distB = Math.abs(y - z);

    if (distA < distB) {
        return "Cat A";
    } else if (distB < distA) {
        return "Cat B";
    } else {
        return "Mouse C"; 
    }
} 
  </pre>

## 📌3 -  Grading Students

<pre> 
  function gradingStudents(grades) {
    let finalGrades = [];

    for (let grade of grades) {
        if (grade < 38) {
            finalGrades.push(grade);
        } else {
            let nextMultiple = Math.ceil(grade / 5) * 5;
            if (nextMultiple - grade < 3) {
                finalGrades.push(nextMultiple);
            } else {
                finalGrades.push(grade);
            }
        }
    }

    return finalGrades;
}

</pre>

## 📌4- Beautiful Days at the Movies

<pre> function beautifulDays(i, j, k) {
    let count = 0;

    for (let day = i; day <= j; day++) {
        // reverse the number
        let reversed = parseInt(day.toString().split('').reverse().join(''));
        // absolute difference
        let diff = Math.abs(day - reversed);

        if (diff % k === 0) {
            count++;
        }
    }

    return count;
} 
      
</pre>

## 📌5 - Breaking the Records 

<pre>
  function breakingRecords(scores) {
    let maxScore = scores[0];
    let minScore = scores[0];
    let maxCount = 0;
    let minCount = 0;

    for (let i = 1; i < scores.length; i++) {
        if (scores[i] > maxScore) {
            maxScore = scores[i];
            maxCount++;
        } else if (scores[i] < minScore) {
            minScore = scores[i];
            minCount++;
        }
    }

    return [maxCount, minCount];
}
                               
</pre>
