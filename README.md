# wpfSnippet

Coleção de Snippets e métodos ágeis para melhor produtividade no desenvolvimento em Windows Presentation Foundation, através de Visual Studio + ReSharper

### Getting started

- [Baixe](https://github.com/dotpegaso/wpfsnippet/archive/master.zip) o arquivo e entre na pasta Snippets
- Abra o `Visual Studio` e em seu menu superior, navegue até `Resharper > Tools > Templates Explorer`
- Em `Scopes` selecione `Global` e clique em `Import`

![alt tag](https://github.com/dotpegaso/wpfsnippet/res/example.gif)

### Estrutura básica

- O comando **controls:** é equivalente à uma estrutura básica de nova janela, use-o sempre que criar um novo arquivo .xaml:
```
<controls:BdsElysiumWindow
x:Class="NAMESPACE.View.**[NOME_DA_TELA]**"
xmlns="http://schemas.microsoft.com/winfx/2006/xaml/presentation"
xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml"
xmlns:mc="http://schemas.openxmlformats.org/markup-compatibility/2006"
xmlns:d="http://schemas.microsoft.com/expression/blend/2008"
xmlns:params="http://schemas.codeplex.com/elysium/params"
xmlns:resources="clr-namespace:Bds.Bdsh.Excel.Vsto.Consult.Resources"
xmlns:controls="clr-namespace:Bds.Bdsh.Excel.Vsto.Consult.Controls"
xmlns:ff="clr-namespace:Bds.Bdsh.Excel.Vsto.Consult.FunctionalFun.UI"
xmlns:extra="http://schemas.extra.com/ui"
xmlns:metro="http://schemas.codeplex.com/elysium"
xmlns:viewModel="clr-namespace:Bds.Bdsh.Excel.Vsto.Consult.ViewModel"
xmlns:utils="clr-namespace:Bds.Bdsh.Excel.Vsto.Consult.Utils"
xmlns:i="http://schemas.microsoft.com/expression/2010/interactivity"
mc:Ignorable="d"
d:DesignHeight="600" d:DesignWidth="800"
Height="600" Width="800"
TitleBarBackground="#FF1F6F43"
params:Design.AccentBrush="#FF1F6F43"
TitleBarForeground="White"
WindowStartupLocation="CenterOwner"
WindowState="Normal"
DataContext="{Binding RelativeSource={RelativeSource Self}, Path=ViewModel, Mode=TwoWay, UpdateSourceTrigger=PropertyChanged}"
Title="{x:Static resources:Resource.**[NOME_DA_TELA]**_TitleBar}">
<!--VOCÊ PODE ALTERAR O TAMANHO DA TELA ACIMA, NA PROPRIEDADE "Height="" Width=""-->
<!--NÃO ESQUEÇA DE INSERIR O NOME DA SUA TELA NAS PROPRIEDADES x:Class="" & Title=""-->

<Grid Margin="5">
    <!--INICIE O CÓDIGO AQUI-->
</Grid>

</controls:BdsElysiumWindow>
```

- Use **gridcd** para:
```
<Grid.ColumnDefinitions>
    <ColumnDefinition Width="**VALOR**" />
</Grid.ColumnDefinitions>
```

- Use **cold** para:
```
<ColumnDefinition Width="**VALOR**" />
```

- Use **gridc** para:
```
<Grid Grid.Column="**VALOR**" Margin="5">
</Grid>
```

- Use **gridrd** para:
```
<Grid.RowDefinitions>
    <RowDefinition Height="**VALOR**" />
</Grid.RowDefinitions>
```

- Use **rowd** para:
```
<RowDefinition Height="**VALOR**" />
```

- Use **gridr** para:
```
<Grid Grid.Row="**VALOR**" Margin="5">
</Grid>
```

- Use **gridrc** para:
```
<Grid Grid.Row="**VALOR**" Grid.Column="**VALOR**" Margin="5">
</Grid>
```

- Use **gridcr** para:
```
<Grid Grid.Column="**VALOR**" Grid.Row="**VALOR**" Margin="5">
</Grid>
```

### Propriedades

  - Use **col** para:
        `Grid.Column="**VALOR**"`

Exemplo
    
    `<Label />` > `<Label col+**TAB** /> **=>** `<Label Grid.Column="**VALOR**"/>` 


  - Use **row** para:
        `Grid.Row="**VALOR**"`

Exemplo
    
    `<Label />` > `<Label row+**TAB** /> **=>** `<Label Grid.Row="**VALOR**"/>`


  - Use **rowcol** para:
        `Grid.Column="**VALOR**"`

Exemplo
    
    `<Label />` > `<Label rowcol+**TAB** /> **=>** `<Label Grid.Row="**VALOR**" Grid.Column="**VALOR**"/>`


  - Use **colrow** para:
        `Grid.Column="**VALOR**"`

Exemplo
    
    `<Label />` > `<Label colrow+**TAB** /> **=>** `<Label Grid.Column="**VALOR**" Grid.Row="**VALOR**"/>`


### Múltiplos

Você também pode criar múltiplos `<Grid.ColumnDefinitions>` e  `<Grid.RowDefinitions>`

Para múltiplas colunas:

- Use **2cold** para:
  ```
<ColumnDefinition Width="**VALOR**" />
<ColumnDefinition Width="**VALOR**" />
  ```

  - Use **3cold** para:
        <ColumnDefinition Width="**VALOR**" />
        <ColumnDefinition Width="**VALOR**" />
        <ColumnDefinition Width="**VALOR**" />

  - Use **4cold** para:
        <ColumnDefinition Width="**VALOR**" />
        <ColumnDefinition Width="**VALOR**" />
        <ColumnDefinition Width="**VALOR**" />
        <ColumnDefinition Width="**VALOR**" />

  - Use **5cold** para:
        <ColumnDefinition Width="**VALOR**" />
        <ColumnDefinition Width="**VALOR**" />
        <ColumnDefinition Width="**VALOR**" />
        <ColumnDefinition Width="**VALOR**" />
        <ColumnDefinition Width="**VALOR**" />

Para múltiplas linhas:

  - Use **2rowd** para:
        <RowDefinition Height="**VALOR**" />
        <RowDefinition Height="**VALOR**" />

  - Use **3rowd** para:
        <RowDefinition Height="**VALOR**" />
        <RowDefinition Height="**VALOR**" />
        <RowDefinition Height="**VALOR**" />

  - Use **4rowd** para:
        <RowDefinition Height="**VALOR**" />
        <RowDefinition Height="**VALOR**" />
        <RowDefinition Height="**VALOR**" />
        <RowDefinition Height="**VALOR**" />

  - Use **5rowd** para:
        <RowDefinition Height="**VALOR**" />
        <RowDefinition Height="**VALOR**" />
        <RowDefinition Height="**VALOR**" />
        <RowDefinition Height="**VALOR**" />
        <RowDefinition Height="**VALOR**" />