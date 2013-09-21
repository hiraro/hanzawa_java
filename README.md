# なにこれ
intを返すメソッドを倍返しにするJavaAgentです.
## 例

    class Test {
	    int return1() {
		    System.out.println("##treturn1##");
		    return 1;
	    }

	    static int return2() {
		    System.out.println("##treturn2##");
		    return 2;
	    }

	    public static void main(String[] args) {
		    Test inst = new Test();
		    System.out.println(inst.return1());
		    System.out.println(return2());
	    }
    }
    
    $ java Test
    ##treturn1##
    1
    ##treturn2##
    2
    
    $ java -javaagent:hanzawa.jar Test
    ##treturn1##
    2
    ##treturn2##
    4
    
# ビルド
    $ mvn install