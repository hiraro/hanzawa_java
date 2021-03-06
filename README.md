# なにこれ
intを返すメソッドを倍返しにするJavaAgentです.
## 例

    class Test {
	    int return1() {
		    System.out.println("## return1 ##");
		    return 1;
	    }

	    static int return2() {
		    System.out.println("## return2 ##");
		    return 2;
	    }

	    public static void main(String[] args) {
		    Test inst = new Test();
		    System.out.println(inst.return1());
		    System.out.println(return2());
	    }
    }
    
    $ java Test
    ## return1 ##
    1
    ## return2 ##
    2
    
    $ java -javaagent:hanzawa.jar Test
    ## return1 ##
    2
    ## return2 ##
    4
    
# ビルド
    $ mvn install
