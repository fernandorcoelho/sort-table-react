# sort-table-react
Uma forma simples de ordenar uma coluna com React.

1) Pegar um array de objetos, que neste caso é o sessionHistory;
2) 
```
const [toggleData, setToggleData] = useState(true);

const sortData = (key) => {
  setToggleData(!toggleData);

  if (toggleData) {
    const sortedTimeObj = sessionHistory.sort((a, b) => (a[key] > b[key]) ? 1 : -1);
    sessionHistory = [...sortedTimeObj];
  }
  if (!toggleData) {
    const sortedTimeObj = sessionHistory.sort((a, b) => (a[key] > b[key]) ? -1 : 1);
    sessionHistory = [...sortedTimeObj];
  }
};
```
