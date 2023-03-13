# Sudoku solver

Napište sudoku solver. Na vstupu dostanete hrací desku s libovolným počtem předvyplněných buněk. Vaším úkolem je vyplnit Sudoku, pokud řešení existuje.

Vaše aplikace musí umět alespoň:

* Interně zareprezentovat sudoku (načítat ze vstupu nemusíte, stačí sudoku předat funkci ve formě matice)
* Najít alespoň jedno řešení (existuje-li) libovolně zadaného sudoku 9x9.

Implementoval jsem sudoku solver který vyřeší sudoku, pokud vyřešit lze. Dále výsledek vypíše do konzole.

Zadané sudoku může být velikosti {n^2 * n^2 | n >= 1}.
Relativně rychle běží do velikosti 16x16, ale 25x25 již nedoběhne pokud je celá matice prázdná.

## Příklad použití

Nahrání solveru:

    $ swipl sudoku.pl

Spuštění solveru
    
    $ sudoku(Matice).

Kde 'Matice' je list listů obsahující vyplněná, nebo nevyplněná políčka.

Příklad prázdné matice k vyřešení.

Matice = [
	[_,_,_, _,_,_, _,_,_],
	[_,_,_, _,_,_, _,_,_],
	[_,_,_, _,_,_, _,_,_],
	
	[_,_,_, _,_,_, _,_,_],
	[_,_,_, _,_,_, _,_,_],
	[_,_,_, _,_,_, _,_,_],
	
	[_,_,_, _,_,_, _,_,_],			
	[_,_,_, _,_,_, _,_,_],
	[_,_,_, _,_,_, _,_,_]]

V políčkách se můžou vyskytovat čísla v rozmezí 1 až n. Kde n je velikost Matice n x n.

Příklad částečně vyplněné matice k vyřešení.

Matice = [
    [_,3,_, 9,1,6, _,_,2],
    [6,5,_, _,_,_, 7,_,_],
    [_,_,7, 2,4,_, _,6,_],

    [_,1,_, _,_,_, _,_,_],
    [_,_,4, 3,_,_, _,8,_],
    [_,_,_, 1,_,_, _,2,_],

    [_,8,1, _,_,_, _,_,3],
    [_,_,_, _,_,_, 2,_,9],
    [_,_,_, _,_,5, _,_,_]]

Matice 4x4.

    Matice = [
    [_,4,1,_],
    [1,_,_,_],
    [_,_,_,2],
    [_,_,3,_]]

Více testovacích příkladů je v souboru.

Všechny sudoku příklady 4x4 - 16x16 se spustí příkazem

    $ testAllSudoku.

Všechny unit testy lze spustit pomocí příkazu

    $ testAllUnitTests.

Všechny test včetně unit testů se spustí pomocí příkazu

    $ testAll.

