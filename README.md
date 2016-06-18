# messageBus

A simple message_bus library

## Usage

A simple usage example:

    import 'package:messageBus/messageBus.dart';
    
    MessageBus mBus = new MessageBus();
    
    class Subscriber() extends EventHandler<String> {
        @override
        handleEvent(String event) {
            print('I got an event: $event');
        }
    }

    main() {
        Subscriber subscriber = new Subscriber();
        mBus.subscribe(String, subscriber);
        mBus.publish('Subscriber will get this');
    }

## Features and bugs

Please file feature requests and bugs at the [issue tracker][tracker].

[tracker]: http://example.com/issues/replaceme
