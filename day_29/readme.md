# Mumbling

## Instructions
- Each char becomes n*chars where n is the index + 1, and the first char is capitalized divided by - instead of space.
- Only alphabets are passed as arguments for the accum(s) funciton
- Example: accum("ZpglnRxqenU") should return "Z-Pp-Ggg-Llll-Nnnnn-Rrrrrr-Xxxxxxx-Qqqqqqqq-Eeeeeeeee-Nnnnnnnnnn-Uuuuuuuuuuu"

## Challenges (0/3) done
- [ ] accum("ZpglnRxqenU") returns "Z-Pp-Ggg-Llll-Nnnnn-Rrrrrr-Xxxxxxx-Qqqqqqqq-Eeeeeeeee-Nnnnnnnnnn-Uuuuuuuuuuu"
- [ ] accum("NyffsGeyylB") returns "N-Yy-Fff-Ffff-Sssss-Gggggg-Eeeeeee-Yyyyyyyy-Yyyyyyyyy-Llllllllll-Bbbbbbbbbbb"
- [ ] accum("MjtkuBovqrU") returns "M-Jj-Ttt-Kkkk-Uuuuu-Bbbbbb-Ooooooo-Vvvvvvvv-Qqqqqqqqq-Rrrrrrrrrr-Uuuuuuuuuuu"

```function accum(s) {
  // your code goes below
  let k, res = '';
  strChar = s.toLowerCase().split('');
  for(let i=0; i<strChar.length; i++) {
      k = i+1;
      let temp = '';
      while(k>0) {
        temp += strChar[i];
        k--;
      }
      temp = capitalFirstLetter(temp);
      res += `${temp}-`
  }

  return res.slice(0, -1);
}


function capitalFirstLetter(str) {
    return str.charAt(0).toUpperCase() + str.slice(1);
}

```
