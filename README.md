# PHPML
language basé sur le html
le PHPML représente une class et une méthode exploité

voici plusieurs formats de PHPML

```html
LE FORMAT LONG :
<phpml actions="class.var" exploite="user" insert="3"></phpml>
OU LE FORMAT REDUIT:
<phpml:class.var="user" insert="3"></phpml>

La partie Actions permet plusieurs possibilité
<phpml:var="user" isert="3"></phpml> cette forme va directement appeler la class phpml et var

si je désire exploité le constructeur avec des drapeaux de la class
je peux donc utilisé @drapeau1#drapeau2
<phpml:class.var@supervar#default_true="user" insert="3"></phpml>

il existe une autre forme
<phpml:class.var(elements)="user" insert="3"></phpml>
cela permet d'exploité visuellement différement des valeurs ou des drapeaux

```
Utilisation : 
ou vous chargez un fichier avec "ctag"
```html
$tag = new Modules_actions();
$tag->ctag( <<<TAG
<phpml:var="user" inserts="$test"></phpml>
<phpml:head="{
'doctype':'html',
'lang':'fr',
'title':'test',
'base':'',
'head':{
    'meta':'',
    'link':[
            {'rel':'alternate', 'href':'https://www.php.net/manual/en/control-structures.if.php', 'hreflang':'en'},
            {'rel':'alternate', 'href':'https://www.php.net/manual/en/control-structures.if.php', 'hreflang':'en'},
            {'rel':'alternate', 'href':'https://www.php.net/manual/en/control-structures.if.php', 'hreflang':'en'}
        ]
    }
}"><script>

</script></phpml>
<phpml:if(user==2)>
    <done>
        <div>test 1</div>
        <div>test 2</div>
        <div>test 3</div>
    </done>
    <elseif(user==3)>
        <div>test 4</div>
        <div>test 5</div>
        <div>test 6</div>
    </elseif>
        <else>
        <div>test 7</div>
        <div>test 8</div>
        <div>test 9</div>
    </else>
</phpml>
<phpml:end><footer></footer></phpml><phpml:var="user" inserts="$test"></phpml>
<phpml:head="{
'doctype':'html',
'lang':'fr',
'title':'test',
'base':'',
'head':{
    'meta':'',
    'link':[
            {'rel':'alternate', 'href':'https://www.php.net/manual/en/control-structures.if.php', 'hreflang':'en'},
            {'rel':'alternate', 'href':'https://www.php.net/manual/en/control-structures.if.php', 'hreflang':'en'},
            {'rel':'alternate', 'href':'https://www.php.net/manual/en/control-structures.if.php', 'hreflang':'en'}
        ]
    }
}"><script>

</script></phpml>
<phpml:if(user==2)>
    <done>
        <div>test 1</div>
        <div>test 2</div>
        <div>test 3</div>
    </done>
    <elseif(user==3)>
        <div>test 4</div>
        <div>test 5</div>
        <div>test 6</div>
    </elseif>
        <else>
        <div>test 7</div>
        <div>test 8</div>
        <div>test 9</div>
    </else>
</phpml>
<phpml:end><footer></footer></phpml>
TAG;
);
```
