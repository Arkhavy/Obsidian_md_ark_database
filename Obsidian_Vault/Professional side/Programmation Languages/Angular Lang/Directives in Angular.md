#Angular

Directives in Angular are Typescript class which is declared with decorator @Directive.

These are the Document Object Model (DOM) Instruction sets, which decide how logic implementation can be done.

You can change the appearance, behavior, or layout of a DOM element using the directives.

Types of Directives:

- Component directive : Used with a template. This type of directive is the most common directive type.

It's nothing but a simple class which is decorated with the @Component decorator.
In Angular, normal typescript class will become a Component class once it has been decorated with @component decorator. It provides additional metadata that determines how the component should be processed, instantiated and used at runtime. It is most commonly used directive in Angular project used to specify the html templates.

- Parameters of Component directive
`Selector` : Tells the template tag which specifies the beginning and end of the component.
`templateURL` : Consists of the template used for the component.
`styleUrls` : It is of array type which consists of all the style format files used for the template.

```Angular
@Component({
	selector: 'app-root',
	templateUrl: './app.component.html',
	styleUrls: ['./app.component.css']
})
```

- Attribute directive : Change the appearance or behavior of an element, component, or another directive.
>Built-ins : NgStyle, NgClass, NgModel

- Structural directive : Change the DOM layout by adding and removing DOM elements.
>Built-ins : NgIf, NgFor, NgSwitch