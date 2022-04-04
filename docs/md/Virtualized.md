### Virtualized

<!--start-code-->

```js
const LargeListsTable = () => {
  const tableRef = React.createRef();
  return (
    <div>
      <Table
        virtualized
        height={400}
        data={fakeLargeData.slice(0, 20)}
        ref={tableRef}
        onRowClick={data => {
          console.log(data);
        }}
      >
        <Column width={70} align="center" fixed>
          <HeaderCell>Id</HeaderCell>
          <Cell dataKey="id" />
            <FooterCell>ID</FooterCell>
        </Column>

        <Column width={130}>
          <HeaderCell>First Name</HeaderCell>
          <Cell dataKey="firstName" />
            <FooterCell>ID</FooterCell>
        </Column>

        <Column width={130}>
          <HeaderCell>Last Name</HeaderCell>
          <Cell dataKey="lastName" />
            <FooterCell>ID</FooterCell>
        </Column>

        <Column width={200}>
          <HeaderCell>City</HeaderCell>
          <Cell dataKey="city" />
            <FooterCell>ID</FooterCell>
        </Column>

        <Column width={200}>
          <HeaderCell>Street</HeaderCell>
          <Cell dataKey="street" />
            <FooterCell>ID</FooterCell>
        </Column>

        <Column minWidth={200} flexGrow={1}>
          <HeaderCell>Company Name</HeaderCell>
          <Cell dataKey="companyName" />
            <FooterCell>ID</FooterCell>
        </Column>
      </Table>
      <button
        onClick={() => {
          tableRef.current.scrollTop(10000);
        }}
      >
        Scroll top
      </button>
    </div>
  );
};

ReactDOM.render(<LargeListsTable />);
```

<!--end-code-->
